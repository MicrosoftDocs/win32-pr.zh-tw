---
description: '[上次儲存的時間/日期摘要] 屬性會在此安裝封裝、轉換或修補套件 modified.Initially 時，將上次儲存的時間/日期摘要屬性值設定為 Null，表示尚未對封裝進行任何變更。 然後，作者應在每次儲存修改的安裝資料庫、轉換或修補套件時，將上次儲存的時間/日期摘要屬性更新為目前的系統時間/日期。'
ms.assetid: be3957fa-463a-4eb2-8b9d-93a16e95a8cf
title: 上次儲存的時間/日期摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe2300640434a52a78575221dc69e0f7263883
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978422"
---
# <a name="last-saved-timedate-summary-property"></a><span data-ttu-id="20c54-104">上次儲存的時間/日期摘要屬性</span><span class="sxs-lookup"><span data-stu-id="20c54-104">Last Saved Time/Date Summary property</span></span>

<span data-ttu-id="20c54-105">[ **上次儲存的時間/日期摘要** ] 屬性會傳達上次修改此安裝套件、轉換或修補套件的時間。</span><span class="sxs-lookup"><span data-stu-id="20c54-105">The **Last Saved Time/Date Summary** property conveys the last time when this installation package, transform, or patch package was modified.</span></span>

<span data-ttu-id="20c54-106">一開始，作者應該將 [ **上次儲存時間/日期摘要** ] 屬性的值設為 Null，表示尚未對封裝進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="20c54-106">Initially, an author should set the value of the **Last Saved Time/Date Summary** property to Null to indicate that no changes have yet been made to the package.</span></span> <span data-ttu-id="20c54-107">然後，作者應在每次儲存修改的安裝資料庫、轉換或修補套件時，將 **上次儲存的時間/日期摘要** 屬性更新為目前的系統時間/日期。</span><span class="sxs-lookup"><span data-stu-id="20c54-107">An author should then update the **Last Saved Time/Date Summary** property to the current system time/date each time a modified installation database, transform, or patch package is saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="20c54-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="20c54-108">Requirements</span></span>



| <span data-ttu-id="20c54-109">需求</span><span class="sxs-lookup"><span data-stu-id="20c54-109">Requirement</span></span> | <span data-ttu-id="20c54-110">值</span><span class="sxs-lookup"><span data-stu-id="20c54-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c54-111">版本</span><span class="sxs-lookup"><span data-stu-id="20c54-111">Version</span></span><br/> | <span data-ttu-id="20c54-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="20c54-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="20c54-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="20c54-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="20c54-114">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="20c54-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20c54-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20c54-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c54-116">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="20c54-116">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




