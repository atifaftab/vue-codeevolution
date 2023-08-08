<template>
    <div>
        <pre>
        {{ JSON.stringify(formValues, null, 2) }}
    </pre>
    </div>

    <form>
        <div>
            <label for="name">Name</label>
            <input type="text" id="name" v-model="formValues.name">
        </div>
        <div>
            <label for="profileSummary">Profile Summary</label>
            <textarea id="profileSummary" v-model="formValues.profileSummary"></textarea>
        </div>
        <div>
            <label for="country">Country</label>
            <select id="country" v-model="formValues.country">
                <option value="">select a country</option>
                <option value="India">India</option>
                <option value="Nepal">Nepal</option>
                <option value="Bhutan">Bhutan</option>
            </select>
        </div>
        <div>
            <label for="jobLocation">Job Location</label>
            <select id="jobLocation" multiple v-model="formValues.jobLocation">
                <option value="India">India</option>
                <option value="UAE">UAE</option>
                <option value="USA">USA</option>
            </select>
        </div>
        <div>
            <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
            <label for="remoteWork">Open to remote work ?</label>
        </div>
        <div>
            <label>Skill Set</label>

            <input type="checkbox" id="java" value="java" v-model="formValues.skillSet">
            <label for="java">JAVA</label>
            <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet">
            <label for="javascript">Javascript</label>
            <input type="checkbox" id="sql" value="sql" v-model="formValues.skillSet">
            <label for="sql">SQL</label>
        </div>
    </form>
</template>
<script>
export default {
    name: 'App',
    data() {
        return {
            formValues: {
                name: '',
                profileSummary: '',
                country: '',
                jobLocation: [],
                remoteWork: "no",
                skillSet: []
            }
        }
    },
    methods: {

    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /* text-align: center; */
    color: #2c3e50;
    margin-top: 60px;
}

.underline {
    text-decoration: underline;
}

.promoted {
    font-style: italic;
}

.new {
    color: olivedrab;
}

.sold-out {
    color: red;
}

label {
    font-weight: bold;
    display: flex;
    margin-bottom: 5px;
}

input+label {
    font-weight: bold;
    display: inline-flex;
    margin-right: 20px;
}

input[type='text'],
textarea,
select {
    display: block;
    width: 400px;
    padding: 6px 12px;
    font-size: 14px;
    line-height: 1.42857143;
    color: #555;
    background-color: #fff;
    background-image: none;
    border: 1px solid #ccc;
    border-radius: 4px;
}
</style>