<template>
    <div class="content">
        <h1 class="c28 c37" id="h.5473ppjvnwhc">
            <span class="c17 c27">CORE -</span>
            <span class="c9 c27 c17">TERMS OF USE</span>
        </h1>
        <h4 class="c28 c38" id="h.rzukxuno5xic">
            <span class="c17 c39">Effective August 25, 2022</span>
        </h4>
        <pre>
            BSD 3-Clause License

            Original Copyright (c) 2020, Ava Labs, Inc.
            All rights reserved.

            Derived Work Since 2023
            Copyright (c) 2023, @REKTBuildr
            All rights reserved.

            Redistribution and use in source and binary forms, with or without
            modification, are permitted provided that the following conditions are met:

            1. Redistributions of source code must retain the above copyright notice, this
            list of conditions and the following disclaimer.

            2. Redistributions in binary form must reproduce the above copyright notice,
            this list of conditions and the following disclaimer in the documentation
            and/or other materials provided with the distribution.

            3. Neither the name of the copyright holder nor the names of its
            contributors may be used to endorse or promote products derived from
            this software without specific prior written permission.

            THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
            AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
            IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
            DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
            FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
            DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
            SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
            CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
            OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
            OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

        </pre>
    </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component
export default class ToSCoreContent extends Vue {}
</script>
<style scoped lang="scss">
.content {
    color: var(--primary-color);

    p {
        opacity: 0.9;
        padding-top: 12pt;
        padding-left: 5pt;
        text-indent: 0pt;
        text-align: justify;
    }

    h1 {
        padding-top: 2pt;
        padding-left: 5pt;
        text-indent: 0pt;
        text-align: justify;
    }

    h4 {
        padding-top: 16pt;
        padding-left: 5pt;
        text-indent: 0pt;
        text-align: justify;
    }

    li {
        margin: 24px 0;
    }
}
</style>
