---
description: '[安全性摘要] 屬性會傳達封裝是否應該以唯讀方式開啟。'
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: 安全性摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978465"
---
# <a name="security-summary-property"></a><span data-ttu-id="e8268-103">安全性摘要屬性</span><span class="sxs-lookup"><span data-stu-id="e8268-103">Security Summary property</span></span>

<span data-ttu-id="e8268-104">[ **安全性摘要** ] 屬性會傳達封裝是否應該以唯讀方式開啟。</span><span class="sxs-lookup"><span data-stu-id="e8268-104">The **Security Summary** property conveys whether the package should be opened as read-only.</span></span> <span data-ttu-id="e8268-105">資料庫編輯工具不應該修改唯讀的強制資料庫，而且應該在嘗試修改唯讀建議的資料庫時發出警告。</span><span class="sxs-lookup"><span data-stu-id="e8268-105">The database editing tool should not modify a read-only enforced database and should issue a warning at attempts to modify a read-only recommended database.</span></span> <span data-ttu-id="e8268-106">這個屬性的下列值適用于 Windows Installer 檔案。</span><span class="sxs-lookup"><span data-stu-id="e8268-106">The following values of this property are applicable to Windows Installer files.</span></span>



| <span data-ttu-id="e8268-107">值</span><span class="sxs-lookup"><span data-stu-id="e8268-107">Value</span></span> | <span data-ttu-id="e8268-108">描述</span><span class="sxs-lookup"><span data-stu-id="e8268-108">Description</span></span>           |
|-------|-----------------------|
| <span data-ttu-id="e8268-109">0</span><span class="sxs-lookup"><span data-stu-id="e8268-109">0</span></span>     | <span data-ttu-id="e8268-110">沒有限制</span><span class="sxs-lookup"><span data-stu-id="e8268-110">No restriction</span></span>        |
| <span data-ttu-id="e8268-111">2</span><span class="sxs-lookup"><span data-stu-id="e8268-111">2</span></span>     | <span data-ttu-id="e8268-112">建議使用唯讀</span><span class="sxs-lookup"><span data-stu-id="e8268-112">Read-only recommended</span></span> |
| <span data-ttu-id="e8268-113">4</span><span class="sxs-lookup"><span data-stu-id="e8268-113">4</span></span>     | <span data-ttu-id="e8268-114">強制唯讀</span><span class="sxs-lookup"><span data-stu-id="e8268-114">Read-only enforced</span></span>    |



 

<span data-ttu-id="e8268-115">這個屬性應該設定為唯讀建議的 (2) 安裝資料庫，以及對轉換或修補程式的唯讀強制 (4) 。</span><span class="sxs-lookup"><span data-stu-id="e8268-115">This property should be set to read-only recommended (2) for an installation database and to read-only enforced (4) for a transform or patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8268-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8268-116">Requirements</span></span>



| <span data-ttu-id="e8268-117">需求</span><span class="sxs-lookup"><span data-stu-id="e8268-117">Requirement</span></span> | <span data-ttu-id="e8268-118">值</span><span class="sxs-lookup"><span data-stu-id="e8268-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8268-119">版本</span><span class="sxs-lookup"><span data-stu-id="e8268-119">Version</span></span><br/> | <span data-ttu-id="e8268-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e8268-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e8268-121">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e8268-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e8268-122">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e8268-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8268-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8268-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8268-124">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="e8268-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




