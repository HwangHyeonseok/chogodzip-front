<template>
    <section class="card card-body border-0 shadow-sm p-4 mb-4" id="room-category">
        <h2 class="h4 mb-4"><i class="fas fa-archive text-primary fs-5 mt-n1 me-2" />시설 정보를 입력해주세요.</h2>

        <div class="row" @input="store.checkFacilitiesInfo">

            <!-- 난방 -->
            <div class="mb-4">
                <label class="form-label d-block fw-bold mb-2 pb-1">난방시설</label>
                <div class="row">
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="h-in-center" v-model="storeFac.facilityHeating.center" >
                      <label class="form-check-label" for="h-in-center">중앙난방</label>
                    </div>
                  </div>
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="h-in-personal" v-model="storeFac.facilityHeating.personal" >
                      <label class="form-check-label" for="h-in-personal">개인난방</label>
                    </div>
                  </div>
                </div>
            </div>

            <!-- 냉방 -->
            <div class="mb-4">
                <label class="form-label d-block fw-bold mb-2 pb-1">냉방시설</label>
                <div class="row">
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="c-in-center" v-model="storeFac.facilityCooling.center">
                      <label class="form-check-label" for="c-in-center">중앙냉방</label>
                    </div>
                  </div>
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="c-in-personal" v-model="storeFac.facilityCooling.personal">
                      <label class="form-check-label" for="c-in-personal">개인냉방</label>
                    </div>
                  </div>
                </div>
            </div>

            <!-- 생활 -->
            <div class="mb-4">
                <label class="form-label d-block fw-bold mb-2 pb-1">생활시설</label>
                <div class="row">
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-bed" v-model="storeFac.facilityLife.bed">
                      <label class="form-check-label" for="l-bed">침대</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-closet" v-model="storeFac.facilityLife.closet">
                      <label class="form-check-label" for="l-closet">옷장(행거)</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-washing-machine" v-model="storeFac.facilityLife.washingMachine">
                      <label class="form-check-label" for="l-washing-machine">세탁기</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-table" v-model="storeFac.facilityLife.table">
                      <label class="form-check-label" for="l-table">식탁</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-micro-wave" v-model="storeFac.facilityLife.microwave">
                      <label class="form-check-label" for="l-micro-wave">전자레인지</label>
                    </div>
                  </div>
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-desk" v-model="storeFac.facilityLife.desk">
                      <label class="form-check-label" for="l-desk">책상</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-refrigerator" v-model="storeFac.facilityLife.refrig">
                      <label class="form-check-label" for="l-refrigerator">냉장고</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-dryer" v-model="storeFac.facilityLife.dryer">
                      <label class="form-check-label" for="l-dryer">건조기</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-air-con" v-model="storeFac.facilityLife.airCon">
                      <label class="form-check-label" for="l-air-con">에어컨</label>
                    </div>
                  </div>
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-chair" v-model="storeFac.facilityLife.chair">
                      <label class="form-check-label" for="l-chair">의자</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-induction" v-model="storeFac.facilityLife.induction">
                      <label class="form-check-label" for="l-induction">인덕션</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-hair-dryer" v-model="storeFac.facilityLife.hairDryer">
                      <label class="form-check-label" for="l-hair-dryer">헤어 드라이기</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="l-tv" v-model="storeFac.facilityLife.tv">
                      <label class="form-check-label" for="l-tv">TV</label>
                    </div>
                  </div>
                </div>
            </div>

            <!-- 안전 -->
            <div class="mb-4">
                <label class="form-label d-block fw-bold mb-2 pb-1">안전시설</label>
                <div class="row">
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="s-digital-lock" v-model="storeFac.facilitySecurity.digitLock">
                      <label class="form-check-label" for="s-digital-lock">디지털도어락</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="s-cctv" v-model="storeFac.facilitySecurity.cctv">
                      <label class="form-check-label" for="s-cctv">CCTV</label>
                    </div>
                  </div>
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="s-fire-killer" v-model="storeFac.facilitySecurity.fireKiller">
                      <label class="form-check-label" for="s-fire-killer">소화기</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="s-spring-cooler" v-model="storeFac.facilitySecurity.springCooler">
                      <label class="form-check-label" for="s-spring-cooler">스프링쿨러</label>
                    </div>
                  </div>
                  <div class="col-sm-4">
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="s-public-entrance" v-model="storeFac.facilitySecurity.publicEntrance">
                      <label class="form-check-label" for="s-public-entrance">공동현관</label>
                    </div>
                    <div class="form-check">
                      <input class="form-check-input" type="checkbox" id="s-fire-alarm" v-model="storeFac.facilitySecurity.fireAlarm">
                      <label class="form-check-label" for="s-fire-alarm">화재 경보 시스템</label>
                    </div>
                  </div>
                </div>
            </div>

        </div>
    </section>
</template>

<script setup>
import { usePostRoomStore } from '@/modules/stores/postRoom';
const store = usePostRoomStore();
const storeFac = store.facilitiesInfo;
</script>