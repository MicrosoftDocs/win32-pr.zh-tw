---
description: LINETERMSHARING \_ 位旗標常數描述可線上路裝置、位址或呼叫之間共用終端機的不同方式。
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: 'LINETERMSHARING_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998769"
---
# <a name="linetermsharing_-constants"></a><span data-ttu-id="7a6d1-103">LINETERMSHARING \_ 常數</span><span class="sxs-lookup"><span data-stu-id="7a6d1-103">LINETERMSHARING\_ Constants</span></span>

<span data-ttu-id="7a6d1-104">**LINETERMSHARING \_** 位旗標常數描述可線上路裝置、位址或呼叫之間共用終端機的不同方式。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-104">The **LINETERMSHARING\_** bit-flag constants describe different ways in which a terminal can be shared between line devices, addresses, or calls.</span></span>

<dl> <dt>

<span data-ttu-id="7a6d1-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ 私用**</span><span class="sxs-lookup"><span data-stu-id="7a6d1-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a6d1-106">終端機裝置是單一線路裝置的私用裝置。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-106">The terminal device is private to a single line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a6d1-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**</span><span class="sxs-lookup"><span data-stu-id="7a6d1-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING\_SHAREDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a6d1-108">終端機裝置可由多行使用。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-108">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="7a6d1-109">各種終端機的 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) 要求最後會在終端機上合併或 conferenced。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-109">The [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) requests of the various terminals end up being merged or conferenced at the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a6d1-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**</span><span class="sxs-lookup"><span data-stu-id="7a6d1-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING\_SHAREDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7a6d1-111">終端機裝置可由多行使用。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-111">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="7a6d1-112">最後一行裝置若要對指定終端機模式的終端機進行 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) 或 [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) ，將會與該模式的終端機獨佔連接。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-112">The last line device to do a [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) or [**TSPI\_lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) to the terminal for a given terminal mode will have exclusive connection to the terminal for that mode.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a6d1-113">備註</span><span class="sxs-lookup"><span data-stu-id="7a6d1-113">Remarks</span></span>

<span data-ttu-id="7a6d1-114">無延伸。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-114">No extensibility.</span></span> <span data-ttu-id="7a6d1-115">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-115">All 32 bits are reserved.</span></span>

<span data-ttu-id="7a6d1-116">這些常數描述可直接線上路裝置與終端機裝置 (（例如電話組) ）之間路由的控制項和資訊資料流程的類別。</span><span class="sxs-lookup"><span data-stu-id="7a6d1-116">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a6d1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a6d1-117">Requirements</span></span>



| <span data-ttu-id="7a6d1-118">需求</span><span class="sxs-lookup"><span data-stu-id="7a6d1-118">Requirement</span></span> | <span data-ttu-id="7a6d1-119">值</span><span class="sxs-lookup"><span data-stu-id="7a6d1-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7a6d1-120">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7a6d1-120">TAPI version</span></span><br/> | <span data-ttu-id="7a6d1-121">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7a6d1-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7a6d1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7a6d1-122">Header</span></span><br/>       | <dl> <span data-ttu-id="7a6d1-123"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="7a6d1-123"><dt>Tapi.h</dt></span></span> </dl> |



 

