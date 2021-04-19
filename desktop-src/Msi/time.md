---
description: Time 屬性是以小時、分鐘和秒為單位的目前時間（以小時、分鐘和秒為單位），格式為 HH： MM： SS （使用24小時制）的常值文字。
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Time 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984329"
---
# <a name="time-property"></a><span data-ttu-id="11759-103">Time 屬性</span><span class="sxs-lookup"><span data-stu-id="11759-103">Time property</span></span>

<span data-ttu-id="11759-104">**Time** 屬性是以小時、分鐘和秒為單位的目前時間（以小時、分鐘和秒為單位），格式為 HH： MM： SS （使用24小時制）的常值文字。</span><span class="sxs-lookup"><span data-stu-id="11759-104">The **Time** property is the current time in hours, minutes, and seconds as a string of literal text in the format HH:MM:SS using a 24 hour clock.</span></span> <span data-ttu-id="11759-105">例如，時間 6:57 p.m。</span><span class="sxs-lookup"><span data-stu-id="11759-105">For example, the time 6:57 p.m.</span></span> <span data-ttu-id="11759-106">以 "18:57:00" 表示。</span><span class="sxs-lookup"><span data-stu-id="11759-106">is represented by "18:57:00".</span></span> <span data-ttu-id="11759-107">值的格式取決於使用者的地區設定，而是使用 [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 函數搭配 time \_ FORCE24HOURFORMAT \| time NOTIMEMARKER 選項取得的格式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="11759-107">The format of the value depends upon the user's locale, and is the format obtained using [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) function with the TIME\_FORCE24HOURFORMAT \| TIME\_NOTIMEMARKER option.</span></span> <span data-ttu-id="11759-108">這個屬性的值是由 Windows Installer 所設定，而不是封裝作者。</span><span class="sxs-lookup"><span data-stu-id="11759-108">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="11759-109">備註</span><span class="sxs-lookup"><span data-stu-id="11759-109">Remarks</span></span>

<span data-ttu-id="11759-110">因為這是文字字串，所以不能用在條件運算式中。</span><span class="sxs-lookup"><span data-stu-id="11759-110">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="11759-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="11759-111">Requirements</span></span>



| <span data-ttu-id="11759-112">需求</span><span class="sxs-lookup"><span data-stu-id="11759-112">Requirement</span></span> | <span data-ttu-id="11759-113">值</span><span class="sxs-lookup"><span data-stu-id="11759-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11759-114">版本</span><span class="sxs-lookup"><span data-stu-id="11759-114">Version</span></span><br/> | <span data-ttu-id="11759-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="11759-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11759-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="11759-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11759-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="11759-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="11759-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="11759-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11759-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11759-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11759-120">屬性</span><span class="sxs-lookup"><span data-stu-id="11759-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 
