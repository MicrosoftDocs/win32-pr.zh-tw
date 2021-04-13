---
title: 放大鏡樣式
description: 本主題說明與 [放大鏡] 控制項搭配使用的樣式。
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384693"
---
# <a name="magnifier-styles"></a><span data-ttu-id="32751-103">放大鏡樣式</span><span class="sxs-lookup"><span data-stu-id="32751-103">Magnifier Styles</span></span>

<span data-ttu-id="32751-104">本主題說明與 [放大鏡] 控制項搭配使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="32751-104">This topic describes the styles used with the magnifier control.</span></span> <span data-ttu-id="32751-105">若要建立放大鏡控制項，請使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式並指定 WC_MAGNIFIER 視窗類別，以及下列放大鏡樣式的組合。</span><span class="sxs-lookup"><span data-stu-id="32751-105">To create a magnifier control, use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function and specify the WC_MAGNIFIER window class, along with a combination of the following magnifier styles.</span></span>

| <span data-ttu-id="32751-106">需求</span><span class="sxs-lookup"><span data-stu-id="32751-106">Requirement</span></span> | <span data-ttu-id="32751-107">值</span><span class="sxs-lookup"><span data-stu-id="32751-107">Value</span></span> |
|:---|:---|
| <span data-ttu-id="32751-108">MS_CLIPAROUNDCURSOR 0x0002L</span><span class="sxs-lookup"><span data-stu-id="32751-108">MS_CLIPAROUNDCURSOR 0x0002L</span></span> | <span data-ttu-id="32751-109">剪住系統游標周圍的 [放大鏡] 視窗區域。</span><span class="sxs-lookup"><span data-stu-id="32751-109">Clips the area of the magnifier window that surrounds the system cursor.</span></span> <span data-ttu-id="32751-110">此樣式可讓使用者查看位於放大鏡視窗後方的螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="32751-110">This style enables the user to see screen content that is behind the magnifier window.</span></span> |
| <span data-ttu-id="32751-111">MS_INVERTCOLORS 0x0004L</span><span class="sxs-lookup"><span data-stu-id="32751-111">MS_INVERTCOLORS 0x0004L</span></span> | <span data-ttu-id="32751-112">使用反向色彩顯示放大的螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="32751-112">Displays the magnified screen content using inverted colors.</span></span> |
| <span data-ttu-id="32751-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span><span class="sxs-lookup"><span data-stu-id="32751-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span></span> | <span data-ttu-id="32751-114">顯示放大的系統游標以及放大的螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="32751-114">Displays the magnified system cursor along with the magnified screen content.</span></span> |

## <a name="requirements"></a><span data-ttu-id="32751-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="32751-115">Requirements</span></span>

| <span data-ttu-id="32751-116">需求</span><span class="sxs-lookup"><span data-stu-id="32751-116">Requirement</span></span> | <span data-ttu-id="32751-117">值</span><span class="sxs-lookup"><span data-stu-id="32751-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="32751-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32751-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32751-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32751-119">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="32751-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32751-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32751-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32751-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="32751-122">標頭</span><span class="sxs-lookup"><span data-stu-id="32751-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="32751-123"><dt>放大。h</dt></span><span class="sxs-lookup"><span data-stu-id="32751-123"><dt>Magnification.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="32751-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32751-124">See also</span></span>

[<span data-ttu-id="32751-125">常數</span><span class="sxs-lookup"><span data-stu-id="32751-125">Constants</span></span>](entry-magapi-constants.md)
