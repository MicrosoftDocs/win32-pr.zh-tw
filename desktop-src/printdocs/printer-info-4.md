---
description: 印表機 \_ 資訊 \_ 4 結構會指定一般印表機資訊。您可以使用此結構來取得 >enumprinters 呼叫的最短印表機資訊。
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: 'PRINTER_INFO_4 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194134"
---
# <a name="printer_info_4-structure"></a><span data-ttu-id="4f8e1-103">印表機 \_ 資訊 \_ 4 結構</span><span class="sxs-lookup"><span data-stu-id="4f8e1-103">PRINTER\_INFO\_4 structure</span></span>

<span data-ttu-id="4f8e1-104">**印表機 \_ 資訊 \_ 4** 結構會指定一般印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-104">The **PRINTER\_INFO\_4** structure specifies general printer information.</span></span>

<span data-ttu-id="4f8e1-105">您可以使用此結構來取得 [**>enumprinters**](enumprinters.md)呼叫的最短印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-105">The structure can be used to retrieve minimal printer information on a call to [**EnumPrinters**](enumprinters.md).</span></span> <span data-ttu-id="4f8e1-106">這種呼叫可讓您快速且輕鬆地取出系統上所有本機安裝印表機的名稱和屬性，以及使用者已建立的所有遠端印表機連線。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-106">Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8e1-107">語法</span><span class="sxs-lookup"><span data-stu-id="4f8e1-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="4f8e1-108">成員</span><span class="sxs-lookup"><span data-stu-id="4f8e1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f8e1-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="4f8e1-110">以 null 結束的字串指標，指定印表機 (本機或遠端) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-110">Pointer to a null-terminated string that specifies the name of the printer (local or remote).</span></span>

</dd> <dt>

<span data-ttu-id="4f8e1-111">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-111">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="4f8e1-112">以 null 結束的字串指標，這是伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-112">Pointer to a null-terminated string that is the name of the server.</span></span>

</dd> <dt>

<span data-ttu-id="4f8e1-113">**屬性**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-113">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="4f8e1-114">指定傳回之資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-114">Specifies information about the returned data.</span></span>



| <span data-ttu-id="4f8e1-115">值</span><span class="sxs-lookup"><span data-stu-id="4f8e1-115">Value</span></span>                       | <span data-ttu-id="4f8e1-116">意義</span><span class="sxs-lookup"><span data-stu-id="4f8e1-116">Meaning</span></span>                          |
|-----------------------------|----------------------------------|
| <span data-ttu-id="4f8e1-117">\_本機印表機屬性 \_</span><span class="sxs-lookup"><span data-stu-id="4f8e1-117">PRINTER\_ATTRIBUTE\_LOCAL</span></span>   | <span data-ttu-id="4f8e1-118">印表機是本機印表機。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-118">The printer is a local printer.</span></span>  |
| <span data-ttu-id="4f8e1-119">印表機 \_ 屬性 \_ 網路</span><span class="sxs-lookup"><span data-stu-id="4f8e1-119">PRINTER\_ATTRIBUTE\_NETWORK</span></span> | <span data-ttu-id="4f8e1-120">印表機是遠端印表機。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-120">The printer is a remote printer.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f8e1-121">備註</span><span class="sxs-lookup"><span data-stu-id="4f8e1-121">Remarks</span></span>

<span data-ttu-id="4f8e1-122">**印表機 \_ 資訊 \_ 4** 結構提供簡單且極快速的方式來抓取本機電腦上安裝的印表機名稱，以及使用者已建立的遠端連線。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-122">The **PRINTER\_INFO\_4** structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="4f8e1-123">使用 **印表機 \_ 資訊 \_ 4** 資料結構呼叫 [**>enumprinters**](enumprinters.md)時，該函式會查詢登錄中的指定資訊，然後立即傳回。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-123">When [**EnumPrinters**](enumprinters.md) is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="4f8e1-124">與其他層級的 **印表機 \_ 資訊 \_ xxx** 資料結構一起呼叫時，這與 **>enumprinters** 的行為不同。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-124">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_xxx** data structures.</span></span> <span data-ttu-id="4f8e1-125">尤其是，使用層級 2 (**印表機 \_ 資訊 \_ 2** ) 資料結構來呼叫 **>enumprinters** 時，它會在每個遠端連線上執行 **OpenPrinter** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-125">In particular, when **EnumPrinters** is called with a level 2 (**PRINTER\_INFO\_2** ) data structure, it performs an **OpenPrinter** call on each remote connection.</span></span> <span data-ttu-id="4f8e1-126">如果遠端連線已關閉，或遠端伺服器已不存在，或遠端印表機已不存在，則函式必須等待 RPC 超時，並導致 **OpenPrinter** 呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-126">If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="4f8e1-127">這可能需要一段時間。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-127">This can take a while.</span></span> <span data-ttu-id="4f8e1-128">傳遞 **印表機 \_ 資訊 \_ 4** 結構，可讓應用程式取出最少的必要資訊; 如果需要更詳細的資訊，則可以進行後續的 **EnumPrinter** 層級2呼叫。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-128">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinter** level 2 call can be made.</span></span>

<span data-ttu-id="4f8e1-129">**屬性** 也可以包含在 [**印表機 \_ 資訊 \_ 2**] 的 [**屬性**] 欄位中定義的值。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-129">**Attributes** can also contain values that are defined in the **Attributes** field of **PRINTER\_INFO\_2**.</span></span>

<span data-ttu-id="4f8e1-130">某些印表機設定（例如，某些非 Windows 列印伺服器的印表機連線）可能會同時傳回 **印表機 \_ 屬性 \_ 本機** 和 **印表機 \_ 屬性 \_ 網路**。</span><span class="sxs-lookup"><span data-stu-id="4f8e1-130">Some printer configurations, such as printer connections to some non-Windows-based print servers, might return both **PRINTER\_ATTRIBUTE\_LOCAL** and **PRINTER\_ATTRIBUTE\_NETWORK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f8e1-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f8e1-131">Requirements</span></span>



| <span data-ttu-id="4f8e1-132">需求</span><span class="sxs-lookup"><span data-stu-id="4f8e1-132">Requirement</span></span> | <span data-ttu-id="4f8e1-133">值</span><span class="sxs-lookup"><span data-stu-id="4f8e1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8e1-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f8e1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8e1-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f8e1-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4f8e1-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f8e1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8e1-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f8e1-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4f8e1-138">標頭</span><span class="sxs-lookup"><span data-stu-id="4f8e1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f8e1-139"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4f8e1-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4f8e1-140">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4f8e1-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4f8e1-141">**\_ 印表機 \_ 資訊 \_ 4W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 4a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4f8e1-141">**\_PRINTER\_INFO\_4W** (Unicode) and **\_PRINTER\_INFO\_4A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="4f8e1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f8e1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8e1-143">列印</span><span class="sxs-lookup"><span data-stu-id="4f8e1-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4f8e1-144">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="4f8e1-144">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4f8e1-145">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-145">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="4f8e1-146">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-146">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="4f8e1-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4f8e1-148">**印表機 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-148">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="4f8e1-149">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-149">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="4f8e1-150">**印表機 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4f8e1-150">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> </dl>

 

 




