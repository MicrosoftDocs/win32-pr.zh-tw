---
description: 本節提供直接操作常數的參考規格。
ms.assetid: 41A828F5-4AE3-4073-89EB-CC1279B9ECED
title: 直接操作常數
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5040191f22e92dcfb8c2ca26edd4080cd4cbb2be
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991792"
---
# <a name="direct-manipulation-constants"></a><span data-ttu-id="b45e8-103">直接操作常數</span><span class="sxs-lookup"><span data-stu-id="b45e8-103">Direct Manipulation Constants</span></span>

<span data-ttu-id="b45e8-104">本節提供 [直接操作](direct-manipulation-portal.md) 常數的參考規格。</span><span class="sxs-lookup"><span data-stu-id="b45e8-104">This section provides the reference specifications for [Direct Manipulation](direct-manipulation-portal.md) constants.</span></span>

| <span data-ttu-id="b45e8-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="b45e8-105">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="b45e8-106">Description</span><span class="sxs-lookup"><span data-stu-id="b45e8-106">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span id="DIRECTMANIPULATION_KEYBOARDFOCUS"></span><span id="directmanipulation_keyboardfocus"></span><dl> <span data-ttu-id="b45e8-107"><dt>**DIRECTMANIPULATION \_KEYBOARDFOCUS**</dt> <dt>0xFFFFFFFE</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-107"><dt>**DIRECTMANIPULATION\_KEYBOARDFOCUS**</dt> <dt>0xFFFFFFFE</dt></span></span> </dl> | <span data-ttu-id="b45e8-108">指定虛擬指標識別碼，以透過鍵盤輸入來模擬觸控連絡人。</span><span class="sxs-lookup"><span data-stu-id="b45e8-108">Specifies a psuedo-pointer ID for emulating a touch contact through keyboard input.</span></span><br/> |
| <span id="DIRECTMANIPULATION_MOUSEFOCUS"></span><span id="directmanipulation_mousefocus"></span><dl> <span data-ttu-id="b45e8-109"><dt>**DIRECTMANIPULATION \_MOUSEFOCUS**</dt> <dt>0xFFFFFFFD</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-109"><dt>**DIRECTMANIPULATION\_MOUSEFOCUS**</dt> <dt>0xFFFFFFFD</dt></span></span> </dl>          | <span data-ttu-id="b45e8-110">指定透過滑鼠輸入模擬觸控連絡人的虛擬指標識別碼。</span><span class="sxs-lookup"><span data-stu-id="b45e8-110">Specifies a psuedo-pointer ID for emulating a touch contact through mouse input.</span></span><br/>    |
| <span id="DIRECTMANIPULATION_MINIMUM_ZOOM"></span><span id="directmanipulation_minimum_zoom"></span><dl> <span data-ttu-id="b45e8-111"><dt>**DIRECTMANIPULATION \_最小 \_ 縮放**</dt> <dt>0.1</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-111"><dt>**DIRECTMANIPULATION\_MINIMUM\_ZOOM**</dt> <dt>0.1</dt></span></span> </dl>          | <span data-ttu-id="b45e8-112">指定10% 允許的最小縮放界限。</span><span class="sxs-lookup"><span data-stu-id="b45e8-112">Specifies the minimum permitted zoom boundary of 10%.</span></span><br/>                               |

## <a name="requirements"></a><span data-ttu-id="b45e8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b45e8-113">Requirements</span></span>

| <span data-ttu-id="b45e8-114">需求</span><span class="sxs-lookup"><span data-stu-id="b45e8-114">Requirement</span></span> | <span data-ttu-id="b45e8-115">值</span><span class="sxs-lookup"><span data-stu-id="b45e8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45e8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b45e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b45e8-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b45e8-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="b45e8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b45e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b45e8-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b45e8-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b45e8-120">Idl</span><span class="sxs-lookup"><span data-stu-id="b45e8-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b45e8-121"><dt>DirectManipulation .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-121"><dt>DirectManipulation.idl</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="b45e8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b45e8-122">See also</span></span>

[<span data-ttu-id="b45e8-123">直接操作參考</span><span class="sxs-lookup"><span data-stu-id="b45e8-123">Direct Manipulation Reference</span></span>](direct-manipulation-reference.md)
