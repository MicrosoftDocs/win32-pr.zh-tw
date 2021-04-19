---
description: 安裝程式會將 UILevel 屬性設定為使用者介面的層級。
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: UILevel 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000800"
---
# <a name="uilevel-property"></a><span data-ttu-id="46019-103">UILevel 屬性</span><span class="sxs-lookup"><span data-stu-id="46019-103">UILevel property</span></span>

<span data-ttu-id="46019-104">安裝程式會將 **UILevel** 屬性設定為使用者介面的層級。</span><span class="sxs-lookup"><span data-stu-id="46019-104">The installer sets the **UILevel** property to the level of the user interface.</span></span> <span data-ttu-id="46019-105">內部 UI 是透過 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)來啟用和設定。</span><span class="sxs-lookup"><span data-stu-id="46019-105">The internal UI is enabled and set by [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="46019-106">這個屬性會設定為下列其中一種 INSTALLUILEVEL 資料類型。</span><span class="sxs-lookup"><span data-stu-id="46019-106">This property is set to one of the following INSTALLUILEVEL data types.</span></span>



| <span data-ttu-id="46019-107">INSTALLUILEVEL</span><span class="sxs-lookup"><span data-stu-id="46019-107">INSTALLUILEVEL</span></span>          | <span data-ttu-id="46019-108">數值</span><span class="sxs-lookup"><span data-stu-id="46019-108">Numeric value</span></span> | <span data-ttu-id="46019-109">使用者介面層級</span><span class="sxs-lookup"><span data-stu-id="46019-109">User interface level</span></span>                        |
|-------------------------|---------------|---------------------------------------------|
| <span data-ttu-id="46019-110">INSTALLUILEVEL \_ 無</span><span class="sxs-lookup"><span data-stu-id="46019-110">INSTALLUILEVEL\_NONE</span></span>    | <span data-ttu-id="46019-111">2</span><span class="sxs-lookup"><span data-stu-id="46019-111">2</span></span>             | <span data-ttu-id="46019-112">完全無訊息安裝。</span><span class="sxs-lookup"><span data-stu-id="46019-112">Completely silent installation.</span></span>             |
| <span data-ttu-id="46019-113">INSTALLUILEVEL \_ 基本</span><span class="sxs-lookup"><span data-stu-id="46019-113">INSTALLUILEVEL\_BASIC</span></span>   | <span data-ttu-id="46019-114">3</span><span class="sxs-lookup"><span data-stu-id="46019-114">3</span></span>             | <span data-ttu-id="46019-115">簡單的進度和錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="46019-115">Simple progress and error handling.</span></span>         |
| <span data-ttu-id="46019-116">INSTALLUILEVEL \_ 縮減</span><span class="sxs-lookup"><span data-stu-id="46019-116">INSTALLUILEVEL\_REDUCED</span></span> | <span data-ttu-id="46019-117">4</span><span class="sxs-lookup"><span data-stu-id="46019-117">4</span></span>             | <span data-ttu-id="46019-118">撰寫的 UI、已隱藏的 wizard 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="46019-118">Authored UI, wizard dialogs suppressed.</span></span>     |
| <span data-ttu-id="46019-119">INSTALLUILEVEL \_ FULL</span><span class="sxs-lookup"><span data-stu-id="46019-119">INSTALLUILEVEL\_FULL</span></span>    | <span data-ttu-id="46019-120">5</span><span class="sxs-lookup"><span data-stu-id="46019-120">5</span></span>             | <span data-ttu-id="46019-121">使用 [嚮導]、[進度]、[錯誤] 撰寫的 UI。</span><span class="sxs-lookup"><span data-stu-id="46019-121">Authored UI with wizards, progress, errors.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="46019-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="46019-122">Requirements</span></span>



| <span data-ttu-id="46019-123">需求</span><span class="sxs-lookup"><span data-stu-id="46019-123">Requirement</span></span> | <span data-ttu-id="46019-124">值</span><span class="sxs-lookup"><span data-stu-id="46019-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46019-125">版本</span><span class="sxs-lookup"><span data-stu-id="46019-125">Version</span></span><br/> | <span data-ttu-id="46019-126">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="46019-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="46019-127">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="46019-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="46019-128">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="46019-128">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="46019-129">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="46019-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46019-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46019-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46019-131">屬性</span><span class="sxs-lookup"><span data-stu-id="46019-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="46019-132">消費者介面</span><span class="sxs-lookup"><span data-stu-id="46019-132">User Interface</span></span>](user-interface.md)
</dt> <dt>

[<span data-ttu-id="46019-133">從自訂動作判斷 UI 層級</span><span class="sxs-lookup"><span data-stu-id="46019-133">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




