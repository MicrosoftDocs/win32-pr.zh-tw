---
description: MSIARPSETTINGSIDENTIFIER 屬性包含以分號分隔的登錄位置清單，應用程式會在其中儲存使用者的設定和喜好設定。
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: MSIARPSETTINGSIDENTIFIER 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999455"
---
# <a name="msiarpsettingsidentifier-property"></a><span data-ttu-id="42cd6-103">MSIARPSETTINGSIDENTIFIER 屬性</span><span class="sxs-lookup"><span data-stu-id="42cd6-103">MSIARPSETTINGSIDENTIFIER property</span></span>

<span data-ttu-id="42cd6-104">**MSIARPSETTINGSIDENTIFIER** 屬性包含以分號分隔的登錄位置清單，應用程式會在其中儲存使用者的設定和喜好設定。</span><span class="sxs-lookup"><span data-stu-id="42cd6-104">The **MSIARPSETTINGSIDENTIFIER** property contains a semi-colon delimited list of the registry locations where the application stores a user's settings and preferences.</span></span> <span data-ttu-id="42cd6-105">在作業系統升級期間，安裝程式可以使用這項資訊來改善正在遷移應用程式之使用者的體驗。</span><span class="sxs-lookup"><span data-stu-id="42cd6-105">During an operating system upgrade, setup can use this information to improve the experience of users who are migrating applications.</span></span>

<span data-ttu-id="42cd6-106">**MSIARPSETTINGSIDENTIFIER** 屬性的值為常值文字，其中包含應用程式儲存其設定的登錄位置清單。</span><span class="sxs-lookup"><span data-stu-id="42cd6-106">The value of the **MSIARPSETTINGSIDENTIFIER** property is literal text that contains the list of registry locations where the application stores its settings.</span></span> <span data-ttu-id="42cd6-107">值可以指定多個可能的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="42cd6-107">The value can specify multiple possible registry locations.</span></span> <span data-ttu-id="42cd6-108">使用分號分隔多個登錄位置。</span><span class="sxs-lookup"><span data-stu-id="42cd6-108">Separate multiple registry locations by using semi-colons.</span></span> <span data-ttu-id="42cd6-109">應用程式設定通常會以下列格式儲存在 **HKCU** 或 **HKLM** 登錄 hive 中： *公司 \\ 應用程式 \\ 版本*。</span><span class="sxs-lookup"><span data-stu-id="42cd6-109">Application settings are typically stored in the **HKCU** or **HKLM** registry hives in the form: *Company\\Application\\Version*.</span></span> <span data-ttu-id="42cd6-110">下列範例是 **MSIARPSETTINGSIDENTIFIER** 屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="42cd6-110">The following example is a possible value for the **MSIARPSETTINGSIDENTIFIER** property.</span></span>

<span data-ttu-id="42cd6-111">*MyCompany \\ AppSuite \\ 1.0;MyCompany \\ App1 \\ 1.0;MyCompany \\ App2 \\ 1。0*</span><span class="sxs-lookup"><span data-stu-id="42cd6-111">*MyCompany\\AppSuite\\1.0;MyCompany\\App1\\1.0;MyCompany\\App2\\1.0*</span></span>

<span data-ttu-id="42cd6-112">這個屬性是選擇性的，可以在 [屬性](property-table.md) 表中設定。</span><span class="sxs-lookup"><span data-stu-id="42cd6-112">This property is optional and can be set in the [Property](property-table.md) table.</span></span> <span data-ttu-id="42cd6-113">如果這個屬性出現在屬性工作表中，則此值不得設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="42cd6-113">If this property appears in the Property table, the value must not be set to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="42cd6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="42cd6-114">Requirements</span></span>



| <span data-ttu-id="42cd6-115">需求</span><span class="sxs-lookup"><span data-stu-id="42cd6-115">Requirement</span></span> | <span data-ttu-id="42cd6-116">值</span><span class="sxs-lookup"><span data-stu-id="42cd6-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42cd6-117">版本</span><span class="sxs-lookup"><span data-stu-id="42cd6-117">Version</span></span><br/> | <span data-ttu-id="42cd6-118">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="42cd6-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="42cd6-119">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="42cd6-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="42cd6-120">Windows Server 2003 或 Windows XP 上的 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="42cd6-120">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="42cd6-121">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="42cd6-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42cd6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42cd6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cd6-123">屬性</span><span class="sxs-lookup"><span data-stu-id="42cd6-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="42cd6-124">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="42cd6-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




