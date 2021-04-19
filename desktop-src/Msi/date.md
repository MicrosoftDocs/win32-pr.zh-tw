---
description: Date 屬性是目前的 month、day 和 year 做為常值文字的字串，格式為 MM/DD/YYYY。
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990705"
---
# <a name="date-property"></a><span data-ttu-id="8b60c-103">Date 屬性</span><span class="sxs-lookup"><span data-stu-id="8b60c-103">Date property</span></span>

<span data-ttu-id="8b60c-104">**Date** 屬性是目前的 month、day 和 year 做為常值文字的字串，格式為 MM/DD/YYYY。</span><span class="sxs-lookup"><span data-stu-id="8b60c-104">The **Date** property is the current month, day, and year as a string of literal text in the format MM/DD/YYYY.</span></span> <span data-ttu-id="8b60c-105">例如，2005年6月22日的日期可以表示為 "06/22/2005"。</span><span class="sxs-lookup"><span data-stu-id="8b60c-105">For example, the date June 22, 2005 can represented as "06/22/2005".</span></span> <span data-ttu-id="8b60c-106">值的格式取決於使用者的地區設定，而是使用 [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) 與 DATE >shortdate 選項取得的格式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8b60c-106">The format of the value depends upon the user's locale, and is the format obtained using [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) with the DATE\_SHORTDATE option.</span></span> <span data-ttu-id="8b60c-107">這個屬性的值是由 Windows Installer 所設定，而不是封裝作者。</span><span class="sxs-lookup"><span data-stu-id="8b60c-107">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b60c-108">備註</span><span class="sxs-lookup"><span data-stu-id="8b60c-108">Remarks</span></span>

<span data-ttu-id="8b60c-109">因為這是文字字串，所以不能用在條件運算式中。</span><span class="sxs-lookup"><span data-stu-id="8b60c-109">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b60c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b60c-110">Requirements</span></span>



| <span data-ttu-id="8b60c-111">需求</span><span class="sxs-lookup"><span data-stu-id="8b60c-111">Requirement</span></span> | <span data-ttu-id="8b60c-112">值</span><span class="sxs-lookup"><span data-stu-id="8b60c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b60c-113">版本</span><span class="sxs-lookup"><span data-stu-id="8b60c-113">Version</span></span><br/> | <span data-ttu-id="8b60c-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8b60c-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8b60c-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8b60c-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8b60c-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="8b60c-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8b60c-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="8b60c-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b60c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b60c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b60c-119">屬性</span><span class="sxs-lookup"><span data-stu-id="8b60c-119">Properties</span></span>](properties.md)
</dt> </dl>

 

