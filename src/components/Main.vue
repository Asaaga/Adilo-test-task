<template>
    <main>
        <div class="content-left">
            <div class="content">
                <img src="https://media.istockphoto.com/photos/video-player-picture-id185213319?k=20&m=185213319&s=612x612&w=0&h=RmU_1k-13vuw0PZjkZ5M3Y_eT6tqcIVTvxjHffXOfLc=" alt="" />
                <span>My Recordings</span>
            </div>
        </div>
        <div class="content-center">
        </div>
        <div class="content-right">
            <div class="snap-title">Snapbyte <i class="fa fa-chevron-right" aria-hidden="true"></i> My Recording </div>
            <div class="buttons-container">
                <div class="content-left-buttons-container">
                    <h4>My Recordings <b class="record-number">25</b></h4>
                </div>
                <div class="content-right-buttons-container">
                    <div class="date-btn">
                        <!-- <i class="fa fa-sort-amount-asc" aria-hidden="true"></i> -->
                        <Button  text="By Date" color="none" textColor="black" />
                    </div>
                    <div class="add-btn">
                        <!-- <i class="fa fa-wifi" aria-hidden="true"></i> -->
                        <Button  text="Add Recode" color="none" textColor="black" />
                    </div>
                    <div class="req-btn">
                        <!-- <i class="fa fa-video-camera" aria-hidden="true"></i> -->
                        <Button  text="New Request" color="none" textColor="white" />
                           
                    </div>
                    <div class="rec-btn">
                        <!-- <i class="fa fa-microphone" aria-hidden="true"></i> -->
                        <Button  text="Start Recording" color="none" textColor="white" />
                    </div>
                </div>
            </div>
            <div class="content-container">
                <table>
                    <tr>
                        <th>Recordings</th>
                        <th>Titles</th>
                        <th></th>
                        <th>Views</th>
                        <th>Size</th>
                        <th>Last Modified</th>
                    </tr>
                    <tr>
                        <td>
                            <video width="320" height="240" controls>
                            <source src="movie.mp4" type="video/mp4">
                            <source src="movie.ogg" type="video/ogg">
                            </video>
                        </td>
                        <td><b>Getting it at the first time</b>
                            <p>Lorem ipsum dolor sit amet consectetur...</p>
                        </td>
                        <td></td>
                        <td>102</td>
                        <td>456KB</td>
                        <td>2 months ago</td>
                    </tr>
                    <tr>
                        <td>
                            <video width="320" height="240" controls>
                            <source src="movie.mp4" type="video/mp4">
                            <source src="movie.ogg" type="video/ogg">
                            </video>
                        </td>
                        <td><b>Getting it at the first time</b>
                            <p>Lorem ipsum dolor sit amet consectetur...</p>
                        </td>
                        <td></td>
                        <td>102</td>
                        <td>456KB</td>
                        <td>2 months ago</td>
                    </tr>
                    <tr>
                        <td>
                            <video width="320" height="240" controls>
                            <source src="movie.mp4" type="video/mp4">
                            <source src="movie.ogg" type="video/ogg">
                            </video>
                        </td>
                        <td><b>Getting it at the first time</b>
                            <p>Lorem ipsum dolor sit amet consectetur...</p>
                        </td>
                        <td></td>
                        <td>102</td>
                        <td>456KB</td>
                        <td>2 months ago</td>
                    </tr>
                </table>
            </div>
        </div>
    </main>
</template>

<script>
    import Button from './Button';

    export default {
        name: 'Main',
        components: {
            Button
        }
    }
</script>

<style scoped>
    main {
        display: flex;
        justify-content: space-between;
    }
    .content-center {
        flex: 1;
    }
    .content-left {
        flex: 3;
        background-color: azure;
        text-align: center;
        margin-left: 20px;
        min-height: 500px;
    }
    .content-left .content {
        border: 1px solid grey;
        border-radius: 10px;
        padding: 5px;
        width: 90%;
        display:flex;
        justify-content: space-around;
        margin: auto;
        align-items: center;
        margin-top: 10px;
    }
    .content img{
        height: 50px;
        width: 50px;
    }
    .content-right {
        flex: 7;
        margin-right: 20px;
    }
    .content-right .snap-title {
        margin-left: 10px; 
        margin-top: 10px;
    }
    .buttons-container {
        display: flex;
    }
    .buttons-container .content-left-buttons-container {
        flex: 4;
        margin-left: 10px;
        margin-top: 10px;
    }
    .content-right-buttons-container {
        flex:6;
        display: flex;
        justify-content: space-between;
    }
    .record-number {
        color: rgb(86, 131, 170);
    }
    table {
        width: 100%;
    }
    td video {
        height: 100px;
        width: 100px;
    }
    .content-container {
        margin-top: 10px;
        display: flex; 
    }
    tr th {
        color:rgb(87, 83, 83);
    }
    td b {
        color:rgb(87, 83, 83);
    }
    .content-right-buttons-container .date-btn {
        background-color: white;
        border-radius: 20px;
        align-items: center;
        height: 50px;
        min-width: 100px;
        display: flex;
        border: 1px solid #aaa !important;
        justify-content: space-around;
    }
    .content-right-buttons-container .add-btn {
        background-color: white;
        border-radius: 20px;
        align-items: center;
        height: 50px;
        min-width: 100px;
        display: flex;
        border: 1px solid #aaa !important;
        justify-content: space-around;
    }
    .content-right-buttons-container .req-btn {
        background-color: rgb(123, 123, 249);
        border-radius: 20px;
        align-items: center;
        height: 50px;
        min-width: 100px;
        display: flex;
        border: 1px solid #aaa !important;
        justify-content: space-around;
    }
    .content-right-buttons-container .rec-btn {
        background-color: rgb(233, 110, 110);
        border-radius: 20px;
        align-items: center;
        height: 50px;
        min-width: 100px;
        display: flex;
        border: 1px solid #aaa !important;
        justify-content: space-around;
        text-align: center;
    }
</style>