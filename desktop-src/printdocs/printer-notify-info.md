---
description: 印表機 \_ 通知 \_ 資訊結構包含 FindNextPrinterChangeNotification 函式所傳回的印表機資訊。 在滿足印表機變更通知物件的等候作業之後，此函數會傳回此資訊。
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: 'PRINTER_NOTIFY_INFO 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987586"
---
# <a name="printer_notify_info-structure"></a><span data-ttu-id="dec41-104">印表機 \_ 通知 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="dec41-104">PRINTER\_NOTIFY\_INFO structure</span></span>

<span data-ttu-id="dec41-105">**印表機 \_ 通知 \_ 資訊** 結構包含 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函式所傳回的印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="dec41-105">The **PRINTER\_NOTIFY\_INFO** structure contains printer information returned by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="dec41-106">在滿足印表機變更通知物件的等候作業之後，此函數會傳回此資訊。</span><span class="sxs-lookup"><span data-stu-id="dec41-106">The function returns this information after a wait operation on a printer change notification object has been satisfied.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec41-107">語法</span><span class="sxs-lookup"><span data-stu-id="dec41-107">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a><span data-ttu-id="dec41-108">成員</span><span class="sxs-lookup"><span data-stu-id="dec41-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dec41-109">**版本**</span><span class="sxs-lookup"><span data-stu-id="dec41-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="dec41-110">此結構的版本。</span><span class="sxs-lookup"><span data-stu-id="dec41-110">The version of this structure.</span></span> <span data-ttu-id="dec41-111">將這個成員設定為2。</span><span class="sxs-lookup"><span data-stu-id="dec41-111">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="dec41-112">**旗標**</span><span class="sxs-lookup"><span data-stu-id="dec41-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="dec41-113">指出通知結構狀態的位旗標。</span><span class="sxs-lookup"><span data-stu-id="dec41-113">A bit flag that indicates the state of the notification structure.</span></span> <span data-ttu-id="dec41-114">如果設定了 [印表機 \_ 通知 \_ 資訊 \_ 已捨棄] 位，則表示必須捨棄某些通知。</span><span class="sxs-lookup"><span data-stu-id="dec41-114">If the PRINTER\_NOTIFY\_INFO\_DISCARDED bit is set, it indicates that some notifications had to be discarded.</span></span>

</dd> <dt>

<span data-ttu-id="dec41-115">**Count**</span><span class="sxs-lookup"><span data-stu-id="dec41-115">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="dec41-116">**AData** 陣列中的 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)元素數目。</span><span class="sxs-lookup"><span data-stu-id="dec41-116">The number of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) elements in the **aData** array.</span></span>

</dd> <dt>

<span data-ttu-id="dec41-117">**aData**</span><span class="sxs-lookup"><span data-stu-id="dec41-117">**aData**</span></span>
</dt> <dd>

<span data-ttu-id="dec41-118">[**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="dec41-118">An array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="dec41-119">陣列的每個元素都會識別單一作業或印表機資訊欄位，並提供該欄位目前的資料。</span><span class="sxs-lookup"><span data-stu-id="dec41-119">Each element of the array identifies a single job or printer information field, and provides the current data for that field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dec41-120">備註</span><span class="sxs-lookup"><span data-stu-id="dec41-120">Remarks</span></span>

<span data-ttu-id="dec41-121">如果 **旗標** 成員具有已設定的印表機 \_ 通知 \_ 資訊 \_ ，則表示發生溢位或錯誤，而且通知可能已遺失。</span><span class="sxs-lookup"><span data-stu-id="dec41-121">If the **Flags** member has the PRINTER\_NOTIFY\_INFO\_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="dec41-122">在此情況下，您必須呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) ，並指定 [印表機通知選項重新整理] \_ 旗標 \_ \_ ，以取得所有目前的資訊。</span><span class="sxs-lookup"><span data-stu-id="dec41-122">In this case, you must call [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) and specify the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag to retrieve all current information.</span></span> <span data-ttu-id="dec41-123">在您要求此重新整理作業之前，系統不會傳送此變更通知物件的其他通知。</span><span class="sxs-lookup"><span data-stu-id="dec41-123">Until you request this refresh operation, the system will not send additional notifications for this change notification object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec41-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="dec41-124">Requirements</span></span>



| <span data-ttu-id="dec41-125">需求</span><span class="sxs-lookup"><span data-stu-id="dec41-125">Requirement</span></span> | <span data-ttu-id="dec41-126">值</span><span class="sxs-lookup"><span data-stu-id="dec41-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec41-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dec41-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dec41-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dec41-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dec41-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dec41-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dec41-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dec41-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dec41-131">標頭</span><span class="sxs-lookup"><span data-stu-id="dec41-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec41-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="dec41-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec41-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dec41-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec41-134">列印</span><span class="sxs-lookup"><span data-stu-id="dec41-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dec41-135">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="dec41-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="dec41-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="dec41-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="dec41-137">**印表機 \_ 通知 \_ 資訊 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="dec41-137">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> </dl>

 

 




