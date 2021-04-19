---
description: 印表機 \_ 資訊 \_ 7 結構會指定目錄服務印表機資訊。
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: 'PRINTER_INFO_7 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988416"
---
# <a name="printer_info_7-structure"></a><span data-ttu-id="8694a-103">印表機 \_ 資訊 \_ 7 結構</span><span class="sxs-lookup"><span data-stu-id="8694a-103">PRINTER\_INFO\_7 structure</span></span>

<span data-ttu-id="8694a-104">**印表機 \_ 資訊 \_ 7** 結構會指定目錄服務印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="8694a-104">The **PRINTER\_INFO\_7** structure specifies directory services printer information.</span></span> <span data-ttu-id="8694a-105">您可以使用此結構搭配 [**SetPrinter**](setprinter.md) 函式，在目錄服務中發佈印表機的資料 (ds) ，或從 ds 更新或移除印表機的已發佈資料。</span><span class="sxs-lookup"><span data-stu-id="8694a-105">Use this structure with the [**SetPrinter**](setprinter.md) function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS.</span></span> <span data-ttu-id="8694a-106">使用此結構搭配 [**GetPrinter**](getprinter.md) 函式來判斷是否已在 DS 中發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="8694a-106">Use this structure with the [**GetPrinter**](getprinter.md) function to determine whether a printer is published in the DS.</span></span>

## <a name="syntax"></a><span data-ttu-id="8694a-107">語法</span><span class="sxs-lookup"><span data-stu-id="8694a-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a><span data-ttu-id="8694a-108">成員</span><span class="sxs-lookup"><span data-stu-id="8694a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8694a-109">**pszObjectGUID**</span><span class="sxs-lookup"><span data-stu-id="8694a-109">**pszObjectGUID**</span></span>
</dt> <dd>

<span data-ttu-id="8694a-110">以 null 結束的字串指標，其中包含與已發行的印表機相關聯之目錄服務列印佇列物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8694a-110">A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer.</span></span> <span data-ttu-id="8694a-111">使用 [**GetPrinter**](getprinter.md) 函式來取得此 GUID。</span><span class="sxs-lookup"><span data-stu-id="8694a-111">Use the [**GetPrinter**](getprinter.md) function to retrieve this GUID.</span></span>

<span data-ttu-id="8694a-112">在呼叫 [**SetPrinter**](setprinter.md)之前，請將 **PszObjectGUID** 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8694a-112">Before calling [**SetPrinter**](setprinter.md), set **pszObjectGUID** to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8694a-113">**dwAction**</span><span class="sxs-lookup"><span data-stu-id="8694a-113">**dwAction**</span></span>
</dt> <dd>

<span data-ttu-id="8694a-114">指出 [**SetPrinter**](setprinter.md) 函式執行的動作。</span><span class="sxs-lookup"><span data-stu-id="8694a-114">Indicates the action for the [**SetPrinter**](setprinter.md) function to perform.</span></span> <span data-ttu-id="8694a-115">若為 [**GetPrinter**](getprinter.md) 函數，這個成員會指出指定的印表機是否已發行。</span><span class="sxs-lookup"><span data-stu-id="8694a-115">For the [**GetPrinter**](getprinter.md) function, this member indicates whether the specified printer is published.</span></span> <span data-ttu-id="8694a-116">這個成員可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="8694a-116">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="8694a-117">值</span><span class="sxs-lookup"><span data-stu-id="8694a-117">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="8694a-118">意義</span><span class="sxs-lookup"><span data-stu-id="8694a-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <span data-ttu-id="8694a-119"><dt>**DSPRINT \_暫**</dt>止的 <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="8694a-119"><dt>**DSPRINT\_PENDING**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="8694a-120">[**GetPrinter**](getprinter.md)：表示系統正在嘗試完成 [**SetPrinter**](setprinter.md) 呼叫所啟動的發行或取消發行作業。</span><span class="sxs-lookup"><span data-stu-id="8694a-120">[**GetPrinter**](getprinter.md): Indicates that the system is attempting to complete a publish or unpublish operation started by a [**SetPrinter**](setprinter.md) call.</span></span><br/> <span data-ttu-id="8694a-121">[**SetPrinter**](setprinter.md)：此值無效。</span><span class="sxs-lookup"><span data-stu-id="8694a-121">[**SetPrinter**](setprinter.md): This value is not valid.</span></span> <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <span data-ttu-id="8694a-122"><dt>**DSPRINT \_發佈**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8694a-122"><dt>**DSPRINT\_PUBLISH**</dt> <dt>0x00000001</dt></span></span> </dl>       | <span data-ttu-id="8694a-123">[**SetPrinter**](setprinter.md)：在 DS 中發佈印表機的資料。</span><span class="sxs-lookup"><span data-stu-id="8694a-123">[**SetPrinter**](setprinter.md): Publishes the printer's data in the DS.</span></span><br/> <span data-ttu-id="8694a-124">[**GetPrinter**](getprinter.md)：表示印表機已發佈。</span><span class="sxs-lookup"><span data-stu-id="8694a-124">[**GetPrinter**](getprinter.md): Indicates the printer is published.</span></span> <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <span data-ttu-id="8694a-125"><dt>**DSPRINT \_重新發佈**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="8694a-125"><dt>**DSPRINT\_REPUBLISH**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="8694a-126">[**SetPrinter**](setprinter.md)：印表機的 DS 資料已解除發佈，然後再次發佈，重新整理已發佈印表機中的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="8694a-126">[**SetPrinter**](setprinter.md): The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="8694a-127">重新發佈也會變更已發行之印表機的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8694a-127">Re-publishing also changes the GUID of the published printer.</span></span><br/> <span data-ttu-id="8694a-128">[**GetPrinter**](getprinter.md)：絕不會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="8694a-128">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <span data-ttu-id="8694a-129"><dt>**DSPRINT \_取消**</dt>發行 <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8694a-129"><dt>**DSPRINT\_UNPUBLISH**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="8694a-130">[**SetPrinter**](setprinter.md)：從 DS 移除印表機的已發佈資料。</span><span class="sxs-lookup"><span data-stu-id="8694a-130">[**SetPrinter**](setprinter.md): Removes the printer's published data from the DS.</span></span><br/> <span data-ttu-id="8694a-131">[**GetPrinter**](getprinter.md)：指出未發佈印表機。</span><span class="sxs-lookup"><span data-stu-id="8694a-131">[**GetPrinter**](getprinter.md): Indicates the printer is not published.</span></span> <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <span data-ttu-id="8694a-132"><dt>**DSPRINT \_UPDATE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8694a-132"><dt>**DSPRINT\_UPDATE**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="8694a-133">[**SetPrinter**](setprinter.md)：更新 DS 中的印表機已發佈資料。</span><span class="sxs-lookup"><span data-stu-id="8694a-133">[**SetPrinter**](setprinter.md): Updates the printer's published data in the DS.</span></span><br/> <span data-ttu-id="8694a-134">[**GetPrinter**](getprinter.md)：絕不會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="8694a-134">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8694a-135">備註</span><span class="sxs-lookup"><span data-stu-id="8694a-135">Remarks</span></span>

<span data-ttu-id="8694a-136">[**SetPrinter**](setprinter.md)呼叫中使用 **印表機資訊 \_ \_ 7** 結構，將印表機資訊發佈到目錄服務。</span><span class="sxs-lookup"><span data-stu-id="8694a-136">The **PRINTER\_INFO\_7** structure is used in a [**SetPrinter**](setprinter.md) call to publish printer information to the directory service.</span></span> <span data-ttu-id="8694a-137">已發佈的資料包含指定之印表機的所有值和資料，可在 SPLDS 多工 \_ 緩衝處理器 \_ 金鑰、SPLDS \_ 驅動程式 \_ 金鑰或 SETPRINTERDATAEX 所建立的 SPLDS \_ 使用者 \_ 金鑰[](setprinterdataex.md)金鑰下找到。</span><span class="sxs-lookup"><span data-stu-id="8694a-137">The published data includes all values and data for the specified printer found under the SPLDS\_SPOOLER\_KEY, SPLDS\_DRIVER\_KEY, or SPLDS\_USER\_KEY keys created by [**SetPrinterDataEx**](setprinterdataex.md).</span></span>

<span data-ttu-id="8694a-138">若為 [**SetPrinter**](setprinter.md)，則應該將 *PszObjectGUID* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8694a-138">For [**SetPrinter**](setprinter.md), *pszObjectGUID* should be set to **NULL**.</span></span> <span data-ttu-id="8694a-139">針對 [**GetPrinter**](getprinter.md)， *pszObjectGUID* 會傳回與已發佈印表機相關聯之目錄服務列印佇列物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8694a-139">For [**GetPrinter**](getprinter.md), *pszObjectGUID* returns the GUID of the directory services print queue object associated with a published printer.</span></span> <span data-ttu-id="8694a-140">您可以使用此 GUID 搭配 Active Directory Services 介面， (ADSI) 方法來取出印表機的已發佈資料。</span><span class="sxs-lookup"><span data-stu-id="8694a-140">You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer.</span></span> <span data-ttu-id="8694a-141">不過，建議用來取得已發佈資料的方法是呼叫 [**GetPrinterDataEx**](getprinterdataex.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="8694a-141">However, the recommended method for retrieving published data is to call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8694a-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="8694a-142">Requirements</span></span>



| <span data-ttu-id="8694a-143">需求</span><span class="sxs-lookup"><span data-stu-id="8694a-143">Requirement</span></span> | <span data-ttu-id="8694a-144">值</span><span class="sxs-lookup"><span data-stu-id="8694a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8694a-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8694a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8694a-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8694a-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8694a-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8694a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8694a-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8694a-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8694a-149">標頭</span><span class="sxs-lookup"><span data-stu-id="8694a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="8694a-150"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8694a-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8694a-151">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="8694a-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8694a-152">**\_ 印表機 \_ 資訊 \_ 7W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 7A** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="8694a-152">**\_PRINTER\_INFO\_7W** (Unicode) and **\_PRINTER\_INFO\_7A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="8694a-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8694a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8694a-154">列印</span><span class="sxs-lookup"><span data-stu-id="8694a-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8694a-155">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="8694a-155">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




