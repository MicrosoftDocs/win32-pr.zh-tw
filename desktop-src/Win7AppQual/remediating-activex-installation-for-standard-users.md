---
description: 修正標準使用者的 ActiveX 安裝相容性問題
ms.assetid: 4199521A-58E6-4475-9B95-A724AB52969A
title: 修正標準使用者的 ActiveX 安裝相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88b26ebd0c6e4887a8a304aeab725b176ee04a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116406"
---
# <a name="fixing-activex-installation-compatibility-issues-for-standard-users"></a><span data-ttu-id="f5b38-103">修正標準使用者的 ActiveX 安裝相容性問題</span><span class="sxs-lookup"><span data-stu-id="f5b38-103">Fixing ActiveX Installation Compatibility Issues for Standard Users</span></span>

<span data-ttu-id="f5b38-104">若要開發安全的桌面環境，您必須減輕惡意 ActiveX 控制項的威脅，並在您的環境中提供適當層級的應用程式相容性。</span><span class="sxs-lookup"><span data-stu-id="f5b38-104">To develop a secure desktop environment, you must mitigate the threats from malicious ActiveX controls and provide an appropriate level of application compatibility in your environment.</span></span> <span data-ttu-id="f5b38-105">*ActiveX 控制項* 是可執行程式碼的一部分 (通常是封裝在封包檔中的 OCX 檔案，) 由 Windows Internet Explorer 安裝和執行。</span><span class="sxs-lookup"><span data-stu-id="f5b38-105">An *ActiveX control* is a piece of executable code (typically an OCX file that is packaged within a cabinet file) that is installed and run through Windows Internet Explorer.</span></span> <span data-ttu-id="f5b38-106">您可以建立 ActiveX 控制項，將功能新增至 web 應用程式，而這些應用程式不容易使用標準的 HTML 程式碼或簡單的腳本來達成。</span><span class="sxs-lookup"><span data-stu-id="f5b38-106">You can create ActiveX controls to add functionality to web applications that you cannot easily achieve by using standard HTML code or a simple script.</span></span>

<span data-ttu-id="f5b38-107">當您遷移至 Windows 7 時，安裝 ActiveX 控制項會成為相容性的問題，並將轉換為標準使用者。</span><span class="sxs-lookup"><span data-stu-id="f5b38-107">Installing ActiveX controls becomes a compatibility issue when your migration to Windows 7 includes a transition to standard users.</span></span> <span data-ttu-id="f5b38-108">這種類型的轉換是 IT 專業人員將其環境移至 [標準使用者帳戶](https://support.microsoft.com/hub/4338813/windows-help)的一般最佳作法。</span><span class="sxs-lookup"><span data-stu-id="f5b38-108">This type of transition is a common best practice in which IT professionals move their environment to a [standard user account](https://support.microsoft.com/hub/4338813/windows-help).</span></span> <span data-ttu-id="f5b38-109">這項轉換不是部署 Windows Internet Explorer 8 的必要條件。</span><span class="sxs-lookup"><span data-stu-id="f5b38-109">This transition is not a requirement for deploying Windows Internet Explorer 8.</span></span>

## <a name="activex-control-installation"></a><span data-ttu-id="f5b38-110">ActiveX 控制項安裝</span><span class="sxs-lookup"><span data-stu-id="f5b38-110">ActiveX Control Installation</span></span>

<span data-ttu-id="f5b38-111">ActiveX 控制項具有簡單的下載和執行部署模型。</span><span class="sxs-lookup"><span data-stu-id="f5b38-111">ActiveX controls have a simple download and execute deployment model.</span></span> <span data-ttu-id="f5b38-112">ActiveX 控制項是透過 HTML **物件** 元素安裝並執行。</span><span class="sxs-lookup"><span data-stu-id="f5b38-112">ActiveX controls are installed and run through the HTML **object** element.</span></span> <span data-ttu-id="f5b38-113">此專案的程式 **代碼基** 底屬性會使用 URL 來指示 Internet Explorer () 如果使用者的電腦上尚未安裝該控制項，則會在該位置取得控制項。</span><span class="sxs-lookup"><span data-stu-id="f5b38-113">The **CODEBASE** attribute on this element tells Internet Explorer (by using a URL) where to get the control if it is not already installed on the user’s machine.</span></span> <span data-ttu-id="f5b38-114">在這種情況下，Internet Explorer 會下載相關聯的安裝套件、在物件上執行信任驗證，並在 Internet Explorer 提示使用者提供安裝許可權。</span><span class="sxs-lookup"><span data-stu-id="f5b38-114">In that case, Internet Explorer downloads the associated installation package, performs trust verification on the object, and prompts the user for installation permission in Internet Explorer.</span></span>

<span data-ttu-id="f5b38-115">在安裝期間，轉譯頁面會註冊並執行控制項。</span><span class="sxs-lookup"><span data-stu-id="f5b38-115">During the installation, the rendering page registers and runs the control.</span></span> <span data-ttu-id="f5b38-116">在安裝控制項之後，任何標準使用者都可以執行控制項。</span><span class="sxs-lookup"><span data-stu-id="f5b38-116">After the control is installed, any standard users can run the control.</span></span> <span data-ttu-id="f5b38-117">這種簡單的散發和執行機制提供簡單的方法，將您的元件散發給 web 應用程式的使用者。</span><span class="sxs-lookup"><span data-stu-id="f5b38-117">This simple mechanism of distribution and execution provides an easy way to distribute your components to users of your web application.</span></span> <span data-ttu-id="f5b38-118">但是標準帳戶使用者無法直接安裝個別電腦的 ActiveX 控制項，而且可能需要系統管理員許可權才能完成安裝。</span><span class="sxs-lookup"><span data-stu-id="f5b38-118">But standard account users cannot directly install per-machine ActiveX controls and they might need administrator privileges to complete the installation.</span></span>

## <a name="activex-installer-service-axis"></a><span data-ttu-id="f5b38-119">ActiveX 安裝程式服務 (軸) </span><span class="sxs-lookup"><span data-stu-id="f5b38-119">ActiveX Installer Service (AXIS)</span></span>

<span data-ttu-id="f5b38-120">ActiveX 安裝程式服務 (AXIS) 可讓您在組織中的電腦上使用群組原則來部署 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="f5b38-120">The ActiveX Installer Service (AXIS) enables you to deploy ActiveX controls by using Group Policy on computers in an organization.</span></span> <span data-ttu-id="f5b38-121">您可以群組原則設定來設定軸，您可以使用群組原則管理主控台 (GPMC) 或本機群組原則編輯器來修改這些設定。</span><span class="sxs-lookup"><span data-stu-id="f5b38-121">You can configure AXIS by Group Policy settings, which you can modify by using the Group Policy Management Console (GPMC) or the Local Group Policy Editor.</span></span>

<span data-ttu-id="f5b38-122">有兩個適用于軸的原則設定：</span><span class="sxs-lookup"><span data-stu-id="f5b38-122">There are two policy settings for AXIS:</span></span>

-   <span data-ttu-id="f5b38-123">[ActiveX 控制項的核准安裝網站] 原則設定是由已核准的安裝網站清單所組成，這些網站是由軸用來判斷是否可以安裝 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="f5b38-123">The Approved Installation Sites for ActiveX Controls policy setting consists of a list of approved installation sites, which the AXIS uses to determine whether an ActiveX control can be installed.</span></span>
-   <span data-ttu-id="f5b38-124">[信任的區域中的網站 ActiveX 安裝原則] 原則設定會識別信任的網站區域如何用來安裝 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="f5b38-124">The ActiveX installation policy for sites in Trusted zones policy setting identifies how Trusted sites zones can be used to install ActiveX controls.</span></span>

<span data-ttu-id="f5b38-125">當網站嘗試安裝 ActiveX 控制項時，該軸會檢查網站的 URL 是否列在已核准的安裝網站清單中，或作為 [信任的網站] 區域的一部分。</span><span class="sxs-lookup"><span data-stu-id="f5b38-125">When a website tries to install an ActiveX control, the AXIS checks to see if the URL of the website is listed in the list of approved installation sites or as part of the trusted sites zone.</span></span> <span data-ttu-id="f5b38-126">如果網站是在其中一個清單中，則軸會確定該網站符合原則所定義的需求。</span><span class="sxs-lookup"><span data-stu-id="f5b38-126">If the site is in either of these lists, the AXIS makes sure that the site meets the requirements that the policy defines.</span></span> <span data-ttu-id="f5b38-127">如果網站和 ActiveX 控制項符合原則設定的所有需求，就會安裝該控制項。</span><span class="sxs-lookup"><span data-stu-id="f5b38-127">If the site and the ActiveX control meet all of the requirements of the policy settings, the control is installed.</span></span> <span data-ttu-id="f5b38-128">如需詳細資訊，請參閱 [管理 ActiveX 安裝程式服務](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="f5b38-128">For more information, see [Administering the ActiveX Installer Service](/previous-versions/windows/it-pro/windows-7/dd631688(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5b38-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5b38-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5b38-130">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="f5b38-130">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
