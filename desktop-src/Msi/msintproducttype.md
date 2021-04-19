---
description: 安裝程式會為 Windows NT、Windows 2000 和更新版本的作業系統設定 MsiNTProductType 屬性。
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: MsiNTProductType 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980114"
---
# <a name="msintproducttype-property"></a><span data-ttu-id="f8fb2-103">MsiNTProductType 屬性</span><span class="sxs-lookup"><span data-stu-id="f8fb2-103">MsiNTProductType property</span></span>

<span data-ttu-id="f8fb2-104">安裝程式會為 Windows NT、Windows 2000 和更新版本的作業系統設定 **MsiNTProductType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-104">The installer sets the **MsiNTProductType** property for Windows NT, Windows 2000, and later operating systems.</span></span> <span data-ttu-id="f8fb2-105">這個屬性工作表示 Windows 產品類型。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-105">This property indicates the Windows product type.</span></span>

<span data-ttu-id="f8fb2-106">若為 Windows 2000 和更新版本的作業系統，安裝程式會設定下列值。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-106">For Windows 2000 and later operating systems, the installer sets the following values.</span></span> <span data-ttu-id="f8fb2-107">請注意，值與 [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)結構的 **wProductType** 欄位相同。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-107">Note that values are the same as of the **wProductType** field of the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span>



| <span data-ttu-id="f8fb2-108">值</span><span class="sxs-lookup"><span data-stu-id="f8fb2-108">Value</span></span> | <span data-ttu-id="f8fb2-109">意義</span><span class="sxs-lookup"><span data-stu-id="f8fb2-109">Meaning</span></span>                                  |
|-------|------------------------------------------|
| <span data-ttu-id="f8fb2-110">1</span><span class="sxs-lookup"><span data-stu-id="f8fb2-110">1</span></span>     | <span data-ttu-id="f8fb2-111">Windows 2000 Professional 和更新版本</span><span class="sxs-lookup"><span data-stu-id="f8fb2-111">Windows 2000 Professional and later</span></span>      |
| <span data-ttu-id="f8fb2-112">2</span><span class="sxs-lookup"><span data-stu-id="f8fb2-112">2</span></span>     | <span data-ttu-id="f8fb2-113">Windows 2000 網域控制站和更新版本</span><span class="sxs-lookup"><span data-stu-id="f8fb2-113">Windows 2000 domain controller and later</span></span> |
| <span data-ttu-id="f8fb2-114">3</span><span class="sxs-lookup"><span data-stu-id="f8fb2-114">3</span></span>     | <span data-ttu-id="f8fb2-115">Windows 2000 伺服器和更新版本</span><span class="sxs-lookup"><span data-stu-id="f8fb2-115">Windows 2000 Server and later</span></span>            |



 

<span data-ttu-id="f8fb2-116">若為 Windows 2000 之前的作業系統，安裝程式會設定下列值。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-116">For operating systems earlier than Windows 2000, the installer sets the following values.</span></span>



| <span data-ttu-id="f8fb2-117">值</span><span class="sxs-lookup"><span data-stu-id="f8fb2-117">Value</span></span> | <span data-ttu-id="f8fb2-118">意義</span><span class="sxs-lookup"><span data-stu-id="f8fb2-118">Meaning</span></span>                      |
|-------|------------------------------|
| <span data-ttu-id="f8fb2-119">1</span><span class="sxs-lookup"><span data-stu-id="f8fb2-119">1</span></span>     | <span data-ttu-id="f8fb2-120">Windows NT 工作站</span><span class="sxs-lookup"><span data-stu-id="f8fb2-120">Windows NT Workstation</span></span>       |
| <span data-ttu-id="f8fb2-121">2</span><span class="sxs-lookup"><span data-stu-id="f8fb2-121">2</span></span>     | <span data-ttu-id="f8fb2-122">Windows NT 網域控制站</span><span class="sxs-lookup"><span data-stu-id="f8fb2-122">Windows NT domain controller</span></span> |
| <span data-ttu-id="f8fb2-123">3</span><span class="sxs-lookup"><span data-stu-id="f8fb2-123">3</span></span>     | <span data-ttu-id="f8fb2-124">Windows NT Server</span><span class="sxs-lookup"><span data-stu-id="f8fb2-124">Windows NT Server</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="f8fb2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8fb2-125">Requirements</span></span>



| <span data-ttu-id="f8fb2-126">需求</span><span class="sxs-lookup"><span data-stu-id="f8fb2-126">Requirement</span></span> | <span data-ttu-id="f8fb2-127">值</span><span class="sxs-lookup"><span data-stu-id="f8fb2-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8fb2-128">版本</span><span class="sxs-lookup"><span data-stu-id="f8fb2-128">Version</span></span><br/> | <span data-ttu-id="f8fb2-129">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f8fb2-130">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f8fb2-131">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-131">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f8fb2-132">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8fb2-132">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8fb2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8fb2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fb2-134">屬性</span><span class="sxs-lookup"><span data-stu-id="f8fb2-134">Properties</span></span>](properties.md)
</dt> </dl>

 

 
