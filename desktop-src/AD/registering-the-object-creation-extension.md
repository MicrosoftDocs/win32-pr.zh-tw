---
title: 註冊物件建立延伸模組
description: 建立 Active Directory Domain Services 中的物件建立延伸模組 DLL 時，必須向 Windows 登錄註冊，並 Active Directory Domain Services，讓 COM 和 Active Directory 的系統管理 MMC 嵌入式管理單元知道此延伸模組。
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933048"
---
# <a name="registering-the-object-creation-extension"></a><span data-ttu-id="fbb64-103">註冊物件建立延伸模組</span><span class="sxs-lookup"><span data-stu-id="fbb64-103">Registering the Object Creation Extension</span></span>

<span data-ttu-id="fbb64-104">建立 Active Directory Domain Services 中的物件建立延伸模組 DLL 時，必須向 Windows 登錄註冊，並 Active Directory Domain Services，讓 COM 和 Active Directory 的系統管理 MMC 嵌入式管理單元知道此延伸模組。</span><span class="sxs-lookup"><span data-stu-id="fbb64-104">When an object creation extension DLL in Active Directory Domain Services is created, it must be registered with the Windows registry and Active Directory Domain Services to make COM and the Active Directory administrative MMC snap-ins aware of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="fbb64-105">在 Windows 登錄中註冊</span><span class="sxs-lookup"><span data-stu-id="fbb64-105">Registering in the Windows Registry</span></span>

<span data-ttu-id="fbb64-106">和所有 COM 伺服器一樣，必須在 Windows 登錄中註冊物件建立延伸模組。</span><span class="sxs-lookup"><span data-stu-id="fbb64-106">Like all COM servers, an object creation extension must be registered in the Windows registry.</span></span> <span data-ttu-id="fbb64-107">此擴充功能會在下列機碼下註冊：</span><span class="sxs-lookup"><span data-stu-id="fbb64-107">The extension is registered under the following key:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

<span data-ttu-id="fbb64-108">" &lt; EXTENSION CLSID &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 CLSID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="fbb64-108">"&lt;extension CLSID&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="fbb64-109">「 &lt; 擴充路徑」 &gt; 包含擴充 DLL 的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="fbb64-109">"&lt;extension path&gt;" contains the path and file name of the extension DLL.</span></span> <span data-ttu-id="fbb64-110">所有物件建立延伸模組的 **>threadingmodel** 值都必須是 "公寓"。</span><span class="sxs-lookup"><span data-stu-id="fbb64-110">The **ThreadingModel** value for all object creation extensions must be "Apartment".</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="fbb64-111">向 Active Directory Domain Services 註冊</span><span class="sxs-lookup"><span data-stu-id="fbb64-111">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="fbb64-112">物件建立延伸模組註冊是一種地區設定特有的。</span><span class="sxs-lookup"><span data-stu-id="fbb64-112">Object creation extension registration is specific to one locale.</span></span> <span data-ttu-id="fbb64-113">如果物件建立延伸模組套用至所有地區設定，它必須在 DisplaySpecifiers 容器中所有地區設定子容器的物件類別 **displaySpecifier** 物件中註冊。</span><span class="sxs-lookup"><span data-stu-id="fbb64-113">If the object creation extension applies to all locales, it must be registered in the object class's **displaySpecifier** object in all of the locale subcontainers in the DisplaySpecifiers container.</span></span> <span data-ttu-id="fbb64-114">如果物件建立延伸模組已針對特定地區設定進行當地語系化，請在該地區設定的 subcontainer 中，將其註冊到 **displaySpecifier** 物件中。</span><span class="sxs-lookup"><span data-stu-id="fbb64-114">If the object creation extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="fbb64-115">如需 DisplaySpecifiers 容器和地區設定的詳細資訊，請參閱 [顯示](display-specifiers.md) 規範和 [DisplaySpecifiers 容器](displayspecifiers-container.md)。</span><span class="sxs-lookup"><span data-stu-id="fbb64-115">For more information about the DisplaySpecifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="fbb64-116">有兩個 DisplaySpecifier 屬性可以在其中註冊物件建立延伸模組。</span><span class="sxs-lookup"><span data-stu-id="fbb64-116">There are two DisplaySpecifier attributes that an object creation extension can be registered under.</span></span> <span data-ttu-id="fbb64-117">這些都是 **creationWizard** 和 **createWizardExt**。</span><span class="sxs-lookup"><span data-stu-id="fbb64-117">These are **creationWizard** and **createWizardExt**.</span></span>

<span data-ttu-id="fbb64-118">**CreationWizard** 屬性會識別主要物件建立延伸模組，以取代 Active Directory 系統管理嵌入式管理單元中的現有或原生物件建立 wizard。主要建立延伸模組會提供第一組頁面，並以與原生頁面相同的方式來主控。</span><span class="sxs-lookup"><span data-stu-id="fbb64-118">The **creationWizard** attribute identifies primary object creation extensions to replace the existing or native object creation wizard in Active Directory administrative snap-ins. A primary creation extension provides the first set of pages and is hosted in the same way as native pages.</span></span> <span data-ttu-id="fbb64-119">這個屬性是單一值，需要下列格式：</span><span class="sxs-lookup"><span data-stu-id="fbb64-119">This attribute is single-valued and requires the following format:</span></span>


```C++
<CLSID>
```



<span data-ttu-id="fbb64-120">" &lt; CLSID &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 COM 物件 CLSID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="fbb64-120">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="fbb64-121">**CreateWizardExt** 屬性會識別次要物件建立延伸模組。</span><span class="sxs-lookup"><span data-stu-id="fbb64-121">The **createWizardExt** attribute identifies secondary object creation extensions.</span></span> <span data-ttu-id="fbb64-122">次要建立延伸模組會將 wizard 頁面新增至原生頁面或主要延伸模組。</span><span class="sxs-lookup"><span data-stu-id="fbb64-122">A secondary creation extension adds wizard pages to the native pages or primary extension.</span></span> <span data-ttu-id="fbb64-123">這個屬性是多重值，需要下列格式：</span><span class="sxs-lookup"><span data-stu-id="fbb64-123">This attribute is multi-valued and requires the following format:</span></span>


```C++
<order number>,<CLSID>
```



<span data-ttu-id="fbb64-124">「 &lt; 訂單編號」 &gt; 是一種不帶正負號的數位，表示頁面在 wizard 中的位置。</span><span class="sxs-lookup"><span data-stu-id="fbb64-124">The "&lt;order number&gt;" is an unsigned number that represents the page's position in the wizard.</span></span> <span data-ttu-id="fbb64-125">顯示建立嚮導時，系統會使用每個值的「訂單編號」比較來排序這些值 &lt; &gt; 。</span><span class="sxs-lookup"><span data-stu-id="fbb64-125">When a creation wizard is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="fbb64-126">如果有一個以上的值具有相同的「 &lt; 訂單編號」 &gt; ，這些頁面會以從 Active Directory 伺服器讀取的順序載入。</span><span class="sxs-lookup"><span data-stu-id="fbb64-126">If more than one value has the same "&lt;order number&gt;", those pages are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="fbb64-127">可能的話，您應該使用非現有的「 &lt; 訂單編號」 &gt; (也就是，屬性) 中的其他值尚未使用的號碼。</span><span class="sxs-lookup"><span data-stu-id="fbb64-127">If possible, you should use a non-existing "&lt;order number&gt;" (that is, one that has not been used by other values in the property).</span></span> <span data-ttu-id="fbb64-128">沒有指定的開始位置，而且「訂單編號」序列中允許有間距 &lt; &gt; 。</span><span class="sxs-lookup"><span data-stu-id="fbb64-128">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="fbb64-129">" &lt; CLSID &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 COM 物件 CLSID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="fbb64-129">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

 

 