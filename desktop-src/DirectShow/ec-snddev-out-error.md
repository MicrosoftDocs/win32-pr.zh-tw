---
description: 音訊轉譯器篩選器中發生裝置錯誤。
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: 'EC_SNDDEV_OUT_ERROR (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1182aaba7bb30ad27511b47ba8e4432d8fd33da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979548"
---
# <a name="ec_snddev_out_error"></a><span data-ttu-id="336e9-103">EC \_ SNDDEV \_ 輸出 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="336e9-103">EC\_SNDDEV\_OUT\_ERROR</span></span>

<span data-ttu-id="336e9-104">音訊轉譯器篩選器中發生裝置錯誤。</span><span class="sxs-lookup"><span data-stu-id="336e9-104">A device error has occurred in an audio renderer filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="336e9-105">參數</span><span class="sxs-lookup"><span data-stu-id="336e9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="336e9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="336e9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="336e9-107">[**SNDDEV \_ 錯誤**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err)列舉類型中的 DWORD 值，指出發生失敗時如何存取裝置。</span><span class="sxs-lookup"><span data-stu-id="336e9-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="336e9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="336e9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="336e9-109">DWORD 值，指出從聲音裝置呼叫傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="336e9-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="336e9-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="336e9-110">Default Action</span></span>

<span data-ttu-id="336e9-111">無。</span><span class="sxs-lookup"><span data-stu-id="336e9-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="336e9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="336e9-112">Requirements</span></span>



| <span data-ttu-id="336e9-113">需求</span><span class="sxs-lookup"><span data-stu-id="336e9-113">Requirement</span></span> | <span data-ttu-id="336e9-114">值</span><span class="sxs-lookup"><span data-stu-id="336e9-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="336e9-115">標頭</span><span class="sxs-lookup"><span data-stu-id="336e9-115">Header</span></span><br/> | <dl> <span data-ttu-id="336e9-116"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="336e9-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="336e9-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="336e9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336e9-118">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="336e9-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="336e9-119">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="336e9-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




