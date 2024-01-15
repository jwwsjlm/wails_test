<script setup>
import HelloWorld from './components/HelloWorld.vue'</script>
import {Exit_app} from '../../wailsjs/go/main/App'
<template>
  <div class="box">
    <div class="title">
      <img class="logo" src="./imgs/logo.png" alt="">
      <span class="tle">Microsoft visual c++ 2015-2022 redistributable 123456789</span>
      <div class="svgbtn">
        <!-- SVG 图标 -->
                        <svg t="1705252587083" class="icon" viewBox="0 0 1024 1024" version="1.1"
                    xmlns="http://www.w3.org/2000/svg" p-id="1032" width="50" height="20">
                    <path
                        d="M810.666667 554.666667H213.333333c-25.6 0-42.666667-17.066667-42.666666-42.666667s17.066667-42.666667 42.666666-42.666667h597.333334c25.6 0 42.666667 17.066667 42.666666 42.666667s-17.066667 42.666667-42.666666 42.666667z"
                        fill="#2c2c2c" p-id="1033"></path>
                </svg>
                <svg t="1705252735745" class="icon" viewBox="0 0 1024 1024" version="1.1"
                    xmlns="http://www.w3.org/2000/svg" p-id="1205" width="50" height="20">
                    <path
                        d="M768 170.666667H256c-46.933333 0-85.333333 38.4-85.333333 85.333333v512c0 46.933333 38.4 85.333333 85.333333 85.333333h512c46.933333 0 85.333333-38.4 85.333333-85.333333V256c0-46.933333-38.4-85.333333-85.333333-85.333333zM256 768V256h512v512H256z"
                        fill="#dbdbdb" p-id="1206"></path>
                </svg>
                <svg t="1705252773811" class="icon" viewBox="0 0 1024 1024" version="1.1"
                    xmlns="http://www.w3.org/2000/svg" p-id="1523" width="50" height="20" @click="closeEvent">
                    <path
                        d="M571.733333 512l247.466667-247.466667c17.066667-17.066667 17.066667-42.666667 0-59.733333s-42.666667-17.066667-59.733333 0L512 452.266667 264.533333 204.8c-17.066667-17.066667-42.666667-17.066667-59.733333 0s-17.066667 42.666667 0 59.733333l247.466667 247.466667-247.466667 247.466667c-17.066667 17.066667-17.066667 42.666667 0 59.733333 8.533333 8.533333 21.333333 12.8 29.866667 12.8s21.333333-4.266667 29.866666-12.8l247.466667-247.466667 247.466667 247.466667c8.533333 8.533333 21.333333 12.8 29.866666 12.8s21.333333-4.266667 29.866667-12.8c17.066667-17.066667 17.066667-42.666667 0-59.733333L571.733333 512z"
                        fill="#2c2c2c" p-id="1524"></path>
                </svg>
      </div>
    </div>
    <div class="content">
      <div class="top">
        <img class="toplogo" src="./imgs/toplogo.png" alt="">
        <div>
          <div class="t left-align">Microsoft visual c++ 2015-2022 redistributable</div>
        </div>
      </div>
      <div class="text">
        <div class="t">Microsoft 软件许可证</div>
        <div class="t">Microsoft visual c++ 2015-2022 redistributable</div>
        <div class="con" v-html="formattedText"></div>
      </div>
      <div class="foot">
        <div class="check">
          <input type="checkbox" id="agree" @click="Checkbox">
    <label for="agree">我同意许可条款和条件（A）</label>
        </div>
        <div class="btn">
          <span class="close">安装(I)</span>
         <span @click="closeEvent">关闭(C)</span> <!-- 给 "关闭" 绑定一个名为 closeEvent 的方法 -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import HelloWorld from "./components/HelloWorld.vue";
import {ExitAppFromGo} from "../wailsjs/go/main/App.js";
import {CheckAgreement} from "../wailsjs/go/main/App.js";

function Checkbox(event){
CheckAgreement(event).then((result) => (
    alert(result)
    ))
}
function closeEvent() {
   ExitAppFromGo().then();
}
export default {
  data() {
    return {
      text: `这些许可条款是 Microsoft Corporation（或您所在地的其中一个关联公司）与您之间达成的协议。 请阅读本条款。 本条款适用于上述软件，包括您用来接收该软件的媒体（如果有）。 本条款也适用于 Microsoft 为该软件提供的任何

后续版本（包括任何更新或补充）、

更新、

补充、

基于 Internet 的服务和

支持服务

，除非上述条款附带有其他条款。 如果确实附带其他条款，则附加条款应适用。

使用该软件，即表示您接受这些条款。如果您不接受这些条款，请不要使用该软件。

如下所述，安装或使用该软件也表示您同意在验证、自动下载和安装某些更新期间传输某些标准计算机信息以便获取基于 Internet 的服务。

如果您遵守这些许可条款，将拥有以下权利。

1.安装和使用权利。

家庭使用。 如果您是家庭用户，则可以在您的个人设备上安装和使用任意数量的本软件副本供您的家庭成员使用。

小型企业。 如果您经营一家小型企业，则最多可以在企业中的十 (10) 台设备上安装和使用本软件。

限制。 本软件不得在政府或学术机构的设备上使用。

组件分离。 该软件的各组件是作为一个整体被授予许可的。 您不得分离这些组件并将其安装在不同的设备上。

包含的 Microsoft 程序。 该软件包含其他 Microsoft 程序。 您使用这些程序时应遵守这些程序的许可条款。

2.基于 Internet 的服务。 Microsoft 随该软件提供基于 Internet 的服务。 可能随时更改或取消这些服务。

同意使用基于 Internet 的服务。 下述以及 Microsoft Security Essentials 隐私声明中的软件功能可通过 Internet 连接到 Microsoft 或服务提供商的计算机系统。 在某些情况下，您不会在连接建立时另外收到通知。 在某些情况下，您可以关闭这些功能或不使用它们。 有关这些功能的详细信息，请参阅 http://go.microsoft.com/fwlink/?LinkId=148744。 使用这些功能，即表示您同意传输此信息。Microsoft 不会将这些信息用于识别您的身份或与您联系。

1.计算机信息。 以下功能使用 Internet 协议，向相应的系统发送计算机信息，例如您的 Internet 协议地址、操作系统类型、浏览器及您使用的软件的名称和版本、安装该软件的设备的语言代码等。 Microsoft 使用此类信息是为了向您提供基于 Internet 的服务。

更新。 默认情况下，该软件将自动下载定义更新。 有关详细信息，请参阅隐私声明，网址为 http://go.microsoft.com/fwlink/?LinkId=148744。

恶意软件删除。 该软件会在定期扫描以及您选择此操作时检查并删除存储在设备中严重程度为高的某些恶意软件（以下简称“恶意软件”）。 该软件在您的设备上检查恶意软件时，会向 Microsoft 发送一份报告，其中包含检测到的任何恶意软件或该软件检查恶意软件时发生的错误、与检测相关的特定信息、该软件之前检查恶意软件时已发生的错误以及设备的其他相关信息，我们可以用这些信息对此产品及其他 Microsoft 产品和服务进行改进。 报告中不包含任何可用来识别您的身份的信息。

可能不需要的软件。 该软件将在您的计算机中搜索严重程度介于低等和中等之间的恶意软件，包括但不限于间谍软件和其他可能不需要的软件（以下简称“可能不需要的软件”）。 只有当您同意时，该软件才会删除或禁用严重程度介于低等和中等之间的可能不需要的软件。 如果其他软件在您的计算机上安装了可能不需要的软件，以此作为您使用其他软件的条件，那么，删除或禁用此可能不需要的软件可能会导致计算机上的其他软件停止工作，并且可能会导致您违反计算机上其他软件的使用许可。 在授权删除此可能不需要的软件之前，您应该先阅读针对其他软件的许可协议。 使用该软件，也可能导致您或系统删除或禁用不属于“可能不需要的软件”的软件。

加入 Microsoft 主动保护服务 (MAPS)。 Microsoft 主动保护服务 (MAPS) 反恶意软件社区是一个包含 Microsoft Security Essentials 用户的自愿参加的全球化社区。 在初始安装时，将默认选择用户加入 MAPS，并成为其基本成员。 如果您具备基本成员资格，则在打开该软件时，MAPS 可以向 Microsoft 报告关于恶意软件以及其他形式的可能不需要的软件的信息。 如果 MAPS 报告包括有关该软件可能能够删除的恶意软件或可能不需要的软件的详细信息，则 MAPS 将下载最新签名对其进行处理。 MAPS 还能够发现“误报”（某项内容最初被确定为恶意软件，结果却并非如此）并解决这些误报问题。 在某些情况下，可能会无意中将个人信息发送到 Microsoft。 但是，Microsoft 不会将这些信息用于识别您的身份或与您联系。 若要了解有关 MAPS 以及此功能传输至 Microsoft 的信息的详细信息，请参阅隐私声明，网址为 http://go.microsoft.com/fwlink/?LinkId=148744。

错误报告。 此软件会自动向 Microsoft 发送错误报告，描述出现错误的软件组件。 该软件不会发送文件或内存转储，除非您选择发送这些内容。 有关错误报告的详细信息，请参阅 http://go.microsoft.com/fwlink/?LinkId=148744。

Windows 更新；Microsoft 更新。 该软件会打开 Windows 更新和 Microsoft 更新的自动更新。 若要使该软件中的 Windows 更新和 Microsoft 更新服务正常工作，将需要时常更新或下载 Windows 更新和/或 Microsoft 更新服务，并且无通知地下载并安装。

2.使用信息。 我们可能会使用计算机信息、错误报告、CEIP 信息和恶意软件报告来改进我们的软件和服务。 我们还可能与其他各方共享这些信息，例如硬件和软件供应商。 他们可能会使用这些信息改进其产品与 Microsoft 软件的兼容性。


3.许可范围。 该软件只是授予许可，并非出售。 本协议只授予您使用该软件的某些权利。 Microsoft 保留所有其他权利。 除非适用的法律赋予您此项限制之外的更多权利，否则您只能在本协议明确许可的范围内使用该软件。 在按规定使用软件时，必须遵守软件中的任何技术限制，这些限制只允许您以特定的方式使用软件。 您不得

绕过该软件中的任何技术限制；

对该软件进行反向工程、反编译或反汇编；尽管有此项限制，但如果适用法律明确许可上述活动，并仅在适用法律明确许可的范围内从事上述活动则不在此限；

制作超过本协议所规定或适用法律（尽管已有本协议的这一限制）所允许数量的软件副本；

发布该软件以便他人复制；

出租、租赁或出借该软件；

向任何第三方转让该软件或本协议；或

使用该软件提供商业软件主机服务。

4.备份副本。您可以制作该软件的一个备份副本。 您只可以用它来重新安装该软件。

5.文档。 任何对您的计算机或内部网络拥有有效访问权限的人都可以为您的内部参考目的而复制和使用文档。

6.转移至另一台设备。 您可以卸载该软件，然后安装到另一台设备上进行使用。 不得通过此方法在多台设备之间共享此许可。

7.出口限制。 相关软件受美国出口法律法规的管辖。 必须遵守适用于该软件的所有国内和国际出口法律和法规。 这些法律包括对目的地、最终用户和最终用途的各种限制。

8.支持服务。 因为该软件按“原样”提供，所以我们可能不为其提供支持服务。

9.完整协议。本协议以及您使用的补充、更新、基于 Internet 的服务和支持服务的有关条款，共同构成了该软件和支持服务的完整协议。

10.适用法律。

美国如果您是在美国购买了该软件，对本协议的解释以及由于违反本协议而引起的索赔均适用华盛顿州法律，不论法律原则是否有冲突。 其他索赔，包括关于各州消费者保护法、反不正当竞争法和侵权法的索赔，均受用户所在州的法律管辖。

美国以外的国家和地区。 如果在任何其他国家/地区获取该软件，将适用该国家/地区的法律。

11.法律效力。 本协议规定了部分法律权利。 根据您所在国家/地区的法律规定，您可能享有其他权利。 您还可能享有与您的软件卖方相关的权利。 如果您所在国家/地区的法律不允许本协议改变您所在国家/地区法律赋予您的权利，则本协议将不改变您按照所在国家/地区的法律应享有的权利。

 12.免责声明。该软件按“原样”授予许可。您自行承担所有使用风险。Microsoft 不提供任何明示的担保、保证或条件。用户可享有其所在地法律赋予的本协议无法变更的其他消费者权利。在您当地法律允许的范围内，Microsoft 排除有关适销性、针对特定目的的适用性和不侵权的默示保证。仅限澳大利亚： 您享有《澳大利亚消费者法》规定的法定保障，这些条款中的任何规定均无意影响这些权利。

补救办法和损害赔偿的限制和排除。您只能因直接损害从 Microsoft 及其供应商处获得退款，且退款金额上限为 5.00 美元。您不能因任何其他损害获得退款，包括后果性的、利润损失、特殊、间接或附带的损害。
此限制适用于

与第三方 Internet 站点上或第三方程序中的软件、服务、内容（包括代码）相关的任何情况；以及

在适用法律许可的范围内就违约、违反保证、担保或条件、严格责任、过失或其他侵权责任所提起的索赔。

即使 Microsoft 知道或应该知道出现损害的可能性，该限制也同样适用。 由于您所在国家/地区可能不允许排除或限制附带的、后果性的或其他损害赔偿责任，上述限制和排除可能不适用于您。`,
    };
  },
  computed: {
    formattedText() {
      return this.text.split(/\n/)
        .map(e => e.trim() ? `<p>${e}</p>` : `</br>`)
        .join('');
    },
  },
  methods: {
  }
};
</script>

<style scoped>
     * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;

    }

    .box {
        overflow: hidden;
        width: 600px;
        height: 374px;
        background-color: #fff;
        border-radius: 10px;
        border: 1px solid #ccc;
      color :#000;
      text-align:left;
    }

    .title {
        background-color: #F0F3F8;
        height: 30px;
        font-size: 16px;
        display: flex;
        align-items: center;
        justify-content: space-around;
        padding: 6px;

    }

    .logo {
        width: 22px;
        height: 22px;
        margin-right: 5px;
    }

    .content {
        padding: 10px 16px;
    }

    .top {
        padding: 5px;
        display: flex;
        font-size: 26px;
        font-weight: 700;
    }

    .toplogo {
        width: 70px;
        height: 70px;
        margin-right: 25px;

    }

    .text {
        width: 100%;
        height: 170px;
        word-break: break-all;
        overflow: auto;
        padding: 10px 2px;
        border: 1px solid #ccc;
        margin-top: 10px;
    }

    .text>.t {
        font-size: 18px;
        font-weight: 700;
        color: #000;
        margin-top: 4px;
    }

    .con {
        margin-top: 10px;
    }

    .check {
        display: flex;
        margin-top: 10px;
        font-size: 14px;
        margin-bottom: 6px;
    }

    .check>input {
        margin-right: 5px;
    }

    .btn {
        font-size: 13px;
        float: right;
    }

    .btn>span {
        display: inline-block;
        border: 1px solid #ccc;
        padding: 3px 16px;
        border-radius: 3px;
        cursor: pointer;
    }

    .svgbtn {
        display: flex;
        align-items: center;
        max-width: 150px;
    }

    svg {
        cursor: pointer;
    }
    .tle{
        white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      text-align: left;
    }



</style>
