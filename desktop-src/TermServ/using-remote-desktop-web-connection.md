---
title: 使用遠端桌面 ActiveX 控制項
description: 如何使用遠端桌面 ActiveX 控制項自訂遠端桌面服務使用者體驗。
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- 使用遠端桌面 ActiveX 控制項遠端桌面服務遠端桌面服務
- 遠端桌面網頁連線遠端桌面服務，使用
- 遠端桌面通訊協定遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966382"
---
# <a name="using-the-remote-desktop-activex-control"></a><span data-ttu-id="04a20-106">使用遠端桌面 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="04a20-106">Using the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="04a20-107">下列主題包含如何使用遠端桌面 ActiveX 控制項自訂遠端桌面服務使用者體驗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="04a20-107">The following topics contain information about how you can use the Remote Desktop ActiveX control to customize the Remote Desktop Services user experience.</span></span>

<span data-ttu-id="04a20-108">您可以使用下列格式的遠端桌面 ActiveX 控制項：</span><span class="sxs-lookup"><span data-stu-id="04a20-108">The Remote Desktop ActiveX control is available in the following forms:</span></span>

-   <span data-ttu-id="04a20-109">可編寫腳本的 **控制項**-可執行可安全編寫腳本的介面。</span><span class="sxs-lookup"><span data-stu-id="04a20-109">**The scriptable control**—implements interfaces that are safe for scripting.</span></span> <span data-ttu-id="04a20-110">這種形式的控制項可供 web 用戶端或腳本 (（例如 VBScript) 主機）使用。</span><span class="sxs-lookup"><span data-stu-id="04a20-110">This form of the control can be used by web clients or scripting (such as VBScript) hosts.</span></span>
-   <span data-ttu-id="04a20-111">**Nonscriptable 控制項**-提供對腳本而言不安全的額外功能。</span><span class="sxs-lookup"><span data-stu-id="04a20-111">**The nonscriptable control**—offers additional functionality that is not safe for scripting.</span></span> <span data-ttu-id="04a20-112">這種形式的控制項可以從原生或 managed 程式碼中使用，但這種表單不能由 web 用戶端或僅限腳本的主機使用。</span><span class="sxs-lookup"><span data-stu-id="04a20-112">This form of the control can be used from native or managed code, but this form cannot be used by web clients or scripting-only hosts.</span></span>

<span data-ttu-id="04a20-113">下列清單針對不同的作業系統版本，包含不同控制項的 **CLSID**。</span><span class="sxs-lookup"><span data-stu-id="04a20-113">The following list contains the **CLSID** s for the different controls for different operating system versions.</span></span> <span data-ttu-id="04a20-114">每個 **CLSID** 都與較新的系統版本相容。</span><span class="sxs-lookup"><span data-stu-id="04a20-114">Each of the **CLSID** s is compatible with later system versions.</span></span> <span data-ttu-id="04a20-115">例如，Windows Vista 上可編寫腳本的控制項 **CLSID** 將可在較新的系統版本上運作，例如 windows 7。</span><span class="sxs-lookup"><span data-stu-id="04a20-115">For example, the **CLSID** for the scriptable control on Windows Vista will work on later system versions, such as Windows 7.</span></span>



| <span data-ttu-id="04a20-116">系統版本</span><span class="sxs-lookup"><span data-stu-id="04a20-116">System version</span></span>                          | <span data-ttu-id="04a20-117">可編寫腳本的控制項 CLSID</span><span class="sxs-lookup"><span data-stu-id="04a20-117">Scriptable control CLSID</span></span>             | <span data-ttu-id="04a20-118">Nonscriptable 控制項 CLSID</span><span class="sxs-lookup"><span data-stu-id="04a20-118">Nonscriptable control CLSID</span></span>          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="04a20-119">Windows 8.1、Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="04a20-119">Windows 8.1, Windows Server 2012 R2</span></span>     | <span data-ttu-id="04a20-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="04a20-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span> | <span data-ttu-id="04a20-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="04a20-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span> |
| <span data-ttu-id="04a20-122">Windows 8、Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04a20-122">Windows 8, Windows Server 2012</span></span>          | <span data-ttu-id="04a20-123">5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="04a20-123">5F681803-2900-4C43-A1CC-CF405404A676</span></span> | <span data-ttu-id="04a20-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="04a20-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span> |
| <span data-ttu-id="04a20-125">Windows 7、Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04a20-125">Windows 7, Windows Server 2008</span></span>          | <span data-ttu-id="04a20-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="04a20-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span> | <span data-ttu-id="04a20-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="04a20-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span> |
| <span data-ttu-id="04a20-128">Windows Vista 包含 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="04a20-128">Windows Vista with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="04a20-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="04a20-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span> | <span data-ttu-id="04a20-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="04a20-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span> |
| <span data-ttu-id="04a20-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04a20-131">Windows Vista</span></span>                           | <span data-ttu-id="04a20-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="04a20-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span> | <span data-ttu-id="04a20-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="04a20-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="04a20-134">本節內容</span><span class="sxs-lookup"><span data-stu-id="04a20-134">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="04a20-135">在網頁中內嵌遠端桌面 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="04a20-135">Embedding the Remote Desktop ActiveX control in a webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

<span data-ttu-id="04a20-136">示範如何使用可編寫腳本之介面的範例。</span><span class="sxs-lookup"><span data-stu-id="04a20-136">Example that demonstrates the use of the scriptable interfaces.</span></span>

</dd> <dt>

[<span data-ttu-id="04a20-137">使用遠端桌面網頁連線來執行可編寫腳本的虛擬通道</span><span class="sxs-lookup"><span data-stu-id="04a20-137">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="04a20-138">示範使用遠端桌面網頁連線執行可編寫腳本之虛擬通道步驟的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="04a20-138">Code examples that show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="04a20-139">使用具有虛擬通道的遠端桌面 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="04a20-139">Using the Remote Desktop ActiveX control with virtual channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="04a20-140">如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，則可以將此應用程式提供給用戶端電腦使用。</span><span class="sxs-lookup"><span data-stu-id="04a20-140">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers.</span></span>

</dd> <dt>

[<span data-ttu-id="04a20-141">遠端桌面 ActiveX 控制項隨附的範例網頁</span><span class="sxs-lookup"><span data-stu-id="04a20-141">Sample webpage included with the Remote Desktop ActiveX control</span></span>](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="04a20-142">遠端桌面網頁連線安裝所在的目錄中 (Default.htm) 的範例網頁。</span><span class="sxs-lookup"><span data-stu-id="04a20-142">A sample webpage (Default.htm) is in the directory where Remote Desktop Web Connection is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="04a20-143">提供 RDP 用戶端安全性</span><span class="sxs-lookup"><span data-stu-id="04a20-143">Providing for RDP client security</span></span>](providing-for-rdp-client-security.md)
</dt> <dd>

<span data-ttu-id="04a20-144">遠端桌面 ActiveX 控制項物件的某些屬性會限制為特定的 Internet Explorer URL 安全性區域。</span><span class="sxs-lookup"><span data-stu-id="04a20-144">Some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span>

</dd> <dt>

[<span data-ttu-id="04a20-145">停用遠端桌面服務功能</span><span class="sxs-lookup"><span data-stu-id="04a20-145">Disabling Remote Desktop Services features</span></span>](disabling-terminal-services-features.md)
</dt> <dd>

<span data-ttu-id="04a20-146">為了加強安全性，您可以選擇停用遠端桌面服務功能。</span><span class="sxs-lookup"><span data-stu-id="04a20-146">For enhanced security, you might choose to disable Remote Desktop Services features.</span></span>

</dd> </dl>

<span data-ttu-id="04a20-147">如需有關安裝遠端桌面 ActiveX 控制項所包含之範例網頁的詳細資訊，請參閱 [遠端桌面 activex 控制項隨附的範例網頁](sample-web-page-included-with-the-remote-desktop-activex-control.md)。</span><span class="sxs-lookup"><span data-stu-id="04a20-147">For more information about the sample webpage that is included with the installation of the Remote Desktop ActiveX control, see [Sample webpage included with the Remote Desktop ActiveX control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 




