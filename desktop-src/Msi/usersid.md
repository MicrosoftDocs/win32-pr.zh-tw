---
description: 安裝程式會將 UserSID 屬性的值設定為執行安裝之使用者的安全識別碼 (SID) 的字串表示。 如需詳細資訊，請參閱授權結構。
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990233"
---
# <a name="usersid-property"></a><span data-ttu-id="77f0d-104">UserSID 屬性</span><span class="sxs-lookup"><span data-stu-id="77f0d-104">UserSID property</span></span>

<span data-ttu-id="77f0d-105">安裝程式會將 **UserSID** 屬性的值設定為執行安裝之使用者的安全識別碼 (SID) 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="77f0d-105">The installer sets the value of the **UserSID** property to the string representation of the security identifier (SID) of the user running the installation.</span></span> <span data-ttu-id="77f0d-106">如需詳細資訊，請參閱 [授權結構](../secauthz/authorization-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="77f0d-106">For more information, see [Authorization Structures](../secauthz/authorization-structures.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="77f0d-107">預設值</span><span class="sxs-lookup"><span data-stu-id="77f0d-107">Default Value</span></span>

<span data-ttu-id="77f0d-108">無。</span><span class="sxs-lookup"><span data-stu-id="77f0d-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="77f0d-109">備註</span><span class="sxs-lookup"><span data-stu-id="77f0d-109">Remarks</span></span>

<span data-ttu-id="77f0d-110">Windows Installer 在 Windows 2000、Windows XP 和 Windows Vista 上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="77f0d-110">The Windows Installer set this property on Windows 2000, Windows XP and Windows Vista.</span></span> <span data-ttu-id="77f0d-111">這個屬性未在所有其他作業系統上定義。</span><span class="sxs-lookup"><span data-stu-id="77f0d-111">This property is not defined on all other operating systems.</span></span>

<span data-ttu-id="77f0d-112">請注意，這個屬性具有可從延遲的自訂動作中取出的特殊屬性。</span><span class="sxs-lookup"><span data-stu-id="77f0d-112">Note that this property has the special attribute that it can be retrieved from a deferred custom action.</span></span> <span data-ttu-id="77f0d-113">以較高許可權執行的自訂動作仍然可以在 **UserSID** 屬性中傳回使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="77f0d-113">A custom action running with elevated privileges can still return the user's SID in **UserSID** property.</span></span> <span data-ttu-id="77f0d-114">如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="77f0d-114">For information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77f0d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="77f0d-115">Requirements</span></span>



| <span data-ttu-id="77f0d-116">需求</span><span class="sxs-lookup"><span data-stu-id="77f0d-116">Requirement</span></span> | <span data-ttu-id="77f0d-117">值</span><span class="sxs-lookup"><span data-stu-id="77f0d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f0d-118">版本</span><span class="sxs-lookup"><span data-stu-id="77f0d-118">Version</span></span><br/> | <span data-ttu-id="77f0d-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="77f0d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="77f0d-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="77f0d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="77f0d-121">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="77f0d-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="77f0d-122">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="77f0d-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77f0d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77f0d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f0d-124">屬性</span><span class="sxs-lookup"><span data-stu-id="77f0d-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 
