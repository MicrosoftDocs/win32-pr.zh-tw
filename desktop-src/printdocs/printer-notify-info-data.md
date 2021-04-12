---
description: 印表機 \_ 通知 \_ 資訊 \_ 資料結構會識別工作或印表機資訊欄位，並提供該欄位目前的資料。
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: 'PRINTER_NOTIFY_INFO_DATA 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193188"
---
# <a name="printer_notify_info_data-structure"></a><span data-ttu-id="42b7c-103">印表機 \_ 通知 \_ 資訊 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="42b7c-103">PRINTER\_NOTIFY\_INFO\_DATA structure</span></span>

<span data-ttu-id="42b7c-104">**印表機 \_ 通知 \_ 資訊 \_ 資料** 結構會識別工作或印表機資訊欄位，並提供該欄位目前的資料。</span><span class="sxs-lookup"><span data-stu-id="42b7c-104">The **PRINTER\_NOTIFY\_INFO\_DATA** structure identifies a job or printer information field and provides the current data for that field.</span></span>

<span data-ttu-id="42b7c-105">[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函式會傳回 [**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md)結構，其中包含 **印表機 \_ 通知 \_ 資訊 \_ 資料** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="42b7c-105">The [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function returns a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of **PRINTER\_NOTIFY\_INFO\_DATA** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b7c-106">語法</span><span class="sxs-lookup"><span data-stu-id="42b7c-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a><span data-ttu-id="42b7c-107">成員</span><span class="sxs-lookup"><span data-stu-id="42b7c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="42b7c-108">**型別**</span><span class="sxs-lookup"><span data-stu-id="42b7c-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-109">指出所提供的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="42b7c-109">Indicates the type of information provided.</span></span> <span data-ttu-id="42b7c-110">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42b7c-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="42b7c-111">值</span><span class="sxs-lookup"><span data-stu-id="42b7c-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="42b7c-112">意義</span><span class="sxs-lookup"><span data-stu-id="42b7c-112">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="42b7c-113"><dt>**作業 \_通知 \_ 類型**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="42b7c-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="42b7c-114">指出 **欄位** 成員指定工作 \_ 通知 \_ 欄位 \_ \* 常數。</span><span class="sxs-lookup"><span data-stu-id="42b7c-114">Indicates that the **Field** member specifies a JOB\_NOTIFY\_FIELD\_\* constant.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="42b7c-115"><dt>**印表機 \_通知 \_ 類型**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="42b7c-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="42b7c-116">指出 **欄位** 成員指定印表機 \_ 通知 \_ 欄位 \_ \* 常數。</span><span class="sxs-lookup"><span data-stu-id="42b7c-116">Indicates that the **Field** member specifies a PRINTER\_NOTIFY\_FIELD\_\* constant.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="42b7c-117">**欄位**</span><span class="sxs-lookup"><span data-stu-id="42b7c-117">**Field**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-118">表示已變更的欄位。</span><span class="sxs-lookup"><span data-stu-id="42b7c-118">Indicates the field that changed.</span></span> <span data-ttu-id="42b7c-119">如需可能值的清單，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="42b7c-119">For a list of possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="42b7c-120">**已保留**</span><span class="sxs-lookup"><span data-stu-id="42b7c-120">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="42b7c-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42b7c-122">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="42b7c-122">**Id**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-123">指出當 **類型** 成員指定工作通知類型時的工作識別碼 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="42b7c-123">Indicates the job identifier if the **Type** member specifies JOB\_NOTIFY\_TYPE.</span></span> <span data-ttu-id="42b7c-124">如果 **類型** 成員指定了 [印表機 \_ 通知類型] \_ ，則這個成員是未定義的。</span><span class="sxs-lookup"><span data-stu-id="42b7c-124">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="42b7c-125">**NotifyData**</span><span class="sxs-lookup"><span data-stu-id="42b7c-125">**NotifyData**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-126">以 **類型** 和 **欄位** 成員為基礎之資料資訊的聯集。</span><span class="sxs-lookup"><span data-stu-id="42b7c-126">A union of data information based on the **Type** and **Field** members.</span></span> <span data-ttu-id="42b7c-127">如需與每個欄位相關聯之資料類型的描述，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="42b7c-127">For a description of the type of data associated with each field, see the Remarks section.</span></span>

<dl> <dt>

<span data-ttu-id="42b7c-128">**adwData \[ 2\]**</span><span class="sxs-lookup"><span data-stu-id="42b7c-128">**adwData\[2\]**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-129">兩個 **DWORD** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="42b7c-129">An array of two **DWORD** values.</span></span> <span data-ttu-id="42b7c-130">對於只使用單一 **DWORD** 的資訊欄位，資料位於 **adwData** \[ 0 \] 。</span><span class="sxs-lookup"><span data-stu-id="42b7c-130">For information fields that use only a single **DWORD**, the data is in **adwData** \[0\].</span></span>

</dd> <dt>

<span data-ttu-id="42b7c-131">**資料**</span><span class="sxs-lookup"><span data-stu-id="42b7c-131">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b7c-132">**cbBuf**</span><span class="sxs-lookup"><span data-stu-id="42b7c-132">**cbBuf**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-133">指出 **pBuf** 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="42b7c-133">Indicates the size, in bytes, of the buffer pointed to by **pBuf**.</span></span>

</dd> <dt>

<span data-ttu-id="42b7c-134">**pBuf**</span><span class="sxs-lookup"><span data-stu-id="42b7c-134">**pBuf**</span></span>
</dt> <dd>

<span data-ttu-id="42b7c-135">包含欄位目前資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="42b7c-135">Pointer to a buffer that contains the field's current data.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42b7c-136">備註</span><span class="sxs-lookup"><span data-stu-id="42b7c-136">Remarks</span></span>

<span data-ttu-id="42b7c-137">如果 **類型** 成員指定 [印表機 \_ 通知 \_ 類型]， **欄位** 成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42b7c-137">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="42b7c-138">欄位</span><span class="sxs-lookup"><span data-stu-id="42b7c-138">Field</span></span></th>
<th><span data-ttu-id="42b7c-139">資料類型</span><span class="sxs-lookup"><span data-stu-id="42b7c-139">Type of data</span></span></th>
<th><span data-ttu-id="42b7c-140">值</span><span class="sxs-lookup"><span data-stu-id="42b7c-140">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42b7c-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="42b7c-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span></span></td>
<td><span data-ttu-id="42b7c-142">不支援。</span><span class="sxs-lookup"><span data-stu-id="42b7c-142">Not supported.</span></span></td>
<td><span data-ttu-id="42b7c-143">0x00</span><span class="sxs-lookup"><span data-stu-id="42b7c-143">0x00</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span><span class="sxs-lookup"><span data-stu-id="42b7c-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span></span></td>
<td><span data-ttu-id="42b7c-145"><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-145"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer.</span></span></td>
<td><span data-ttu-id="42b7c-146">0x01</span><span class="sxs-lookup"><span data-stu-id="42b7c-146">0x01</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span><span class="sxs-lookup"><span data-stu-id="42b7c-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span></span></td>
<td><span data-ttu-id="42b7c-148"><strong>pBuf</strong> 是以 null 結束的字串指標，可識別印表機的共用點。</span><span class="sxs-lookup"><span data-stu-id="42b7c-148"><strong>pBuf</strong> is a pointer to a null-terminated string that identifies the share point for the printer.</span></span></td>
<td><span data-ttu-id="42b7c-149">0x02</span><span class="sxs-lookup"><span data-stu-id="42b7c-149">0x02</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span><span class="sxs-lookup"><span data-stu-id="42b7c-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span></span></td>
<td><span data-ttu-id="42b7c-151"><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含列印工作將列印到的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-151"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to.</span></span> <span data-ttu-id="42b7c-152">如果 &quot; 選取 [印表機共用] &quot; ，這是以逗號分隔的埠清單。</span><span class="sxs-lookup"><span data-stu-id="42b7c-152">If &quot;Printer Pooling&quot; is selected, this is a comma separated list of ports.</span></span></td>
<td><span data-ttu-id="42b7c-153">0x03</span><span class="sxs-lookup"><span data-stu-id="42b7c-153">0x03</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span><span class="sxs-lookup"><span data-stu-id="42b7c-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span></span></td>
<td><span data-ttu-id="42b7c-155"><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含印表機驅動程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-155"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer's driver.</span></span></td>
<td><span data-ttu-id="42b7c-156">0x04</span><span class="sxs-lookup"><span data-stu-id="42b7c-156">0x04</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-157">PRINTER_NOTIFY_FIELD_COMMENT</span><span class="sxs-lookup"><span data-stu-id="42b7c-157">PRINTER_NOTIFY_FIELD_COMMENT</span></span></td>
<td><span data-ttu-id="42b7c-158"><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含新的批註字串，通常是印表機的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="42b7c-158"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</span></span></td>
<td><span data-ttu-id="42b7c-159">0x05</span><span class="sxs-lookup"><span data-stu-id="42b7c-159">0x05</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-160">PRINTER_NOTIFY_FIELD_LOCATION</span><span class="sxs-lookup"><span data-stu-id="42b7c-160">PRINTER_NOTIFY_FIELD_LOCATION</span></span></td>
<td><span data-ttu-id="42b7c-161"><strong>pBuf</strong> 是以 null 結束的字串指標，其中包含印表機的新實體位置 (例如 &quot; Bldg。</span><span class="sxs-lookup"><span data-stu-id="42b7c-161"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new physical location of the printer (for example, &quot;Bldg.</span></span> <span data-ttu-id="42b7c-162">38，房間 1164 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="42b7c-162">38, Room 1164&quot;).</span></span></td>
<td><span data-ttu-id="42b7c-163">0x06</span><span class="sxs-lookup"><span data-stu-id="42b7c-163">0x06</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-164">PRINTER_NOTIFY_FIELD_DEVMODE</span><span class="sxs-lookup"><span data-stu-id="42b7c-164">PRINTER_NOTIFY_FIELD_DEVMODE</span></span></td>
<td><span data-ttu-id="42b7c-165"><strong>pBuf</strong> 是 <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> 結構的指標，可定義預設印表機資料，例如紙張方向和解析度。</span><span class="sxs-lookup"><span data-stu-id="42b7c-165"><strong>pBuf</strong> is a pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> structure that defines default printer data such as the paper orientation and the resolution.</span></span></td>
<td><span data-ttu-id="42b7c-166">0x07</span><span class="sxs-lookup"><span data-stu-id="42b7c-166">0x07</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-167">PRINTER_NOTIFY_FIELD_SEPFILE</span><span class="sxs-lookup"><span data-stu-id="42b7c-167">PRINTER_NOTIFY_FIELD_SEPFILE</span></span></td>
<td><span data-ttu-id="42b7c-168"><strong>pBuf</strong> 是以 null 結束的字串指標，可指定用來建立分隔符號頁面的檔案名。</span><span class="sxs-lookup"><span data-stu-id="42b7c-168"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="42b7c-169">此頁面是用來分隔傳送至印表機的列印工作。</span><span class="sxs-lookup"><span data-stu-id="42b7c-169">This page is used to separate print jobs sent to the printer.</span></span></td>
<td><span data-ttu-id="42b7c-170">0x08</span><span class="sxs-lookup"><span data-stu-id="42b7c-170">0x08</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="42b7c-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span></span></td>
<td><span data-ttu-id="42b7c-172"><strong>pBuf</strong> 是以 null 結束的字串指標，可指定印表機所使用的列印處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-172"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span></td>
<td><span data-ttu-id="42b7c-173">0x09</span><span class="sxs-lookup"><span data-stu-id="42b7c-173">0x09</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42b7c-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span></span></td>
<td><span data-ttu-id="42b7c-175"><strong>pBuf</strong> 是以 null 結束的字串指標，可指定預設的列印處理器參數。</span><span class="sxs-lookup"><span data-stu-id="42b7c-175"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the default print-processor parameters.</span></span></td>
<td><span data-ttu-id="42b7c-176">0x0A</span><span class="sxs-lookup"><span data-stu-id="42b7c-176">0x0A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-177">PRINTER_NOTIFY_FIELD_DATATYPE</span><span class="sxs-lookup"><span data-stu-id="42b7c-177">PRINTER_NOTIFY_FIELD_DATATYPE</span></span></td>
<td><span data-ttu-id="42b7c-178"><strong>pBuf</strong> 是以 null 結束的字串指標，可指定用來記錄列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="42b7c-178"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the data type used to record the print job.</span></span></td>
<td><span data-ttu-id="42b7c-179">0x0B</span><span class="sxs-lookup"><span data-stu-id="42b7c-179">0x0B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="42b7c-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span></span></td>
<td><span data-ttu-id="42b7c-181"><strong>pBuf</strong> 是印表機 <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="42b7c-181"><strong>pBuf</strong> is a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> structure for the printer.</span></span> <span data-ttu-id="42b7c-182">如果沒有安全描述項，指標可能會是 <strong>Null</strong> 。</span><span class="sxs-lookup"><span data-stu-id="42b7c-182">The pointer may be <strong>NULL</strong> if there is no security descriptor.</span></span></td>
<td><span data-ttu-id="42b7c-183">0x0C</span><span class="sxs-lookup"><span data-stu-id="42b7c-183">0x0C</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="42b7c-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span></span></td>
<td><span data-ttu-id="42b7c-185"><strong>adwData</strong> [0] 指定印表機屬性，它可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="42b7c-185"><strong>adwData</strong> [0] specifies the printer attributes, which can be one of the following values:</span></span><dl> <span data-ttu-id="42b7c-186">PRINTER_ATTRIBUTE_QUEUED</span><span class="sxs-lookup"><span data-stu-id="42b7c-186">PRINTER_ATTRIBUTE_QUEUED</span></span><br />
<span data-ttu-id="42b7c-187">PRINTER_ATTRIBUTE_DIRECT</span><span class="sxs-lookup"><span data-stu-id="42b7c-187">PRINTER_ATTRIBUTE_DIRECT</span></span><br />
<span data-ttu-id="42b7c-188">PRINTER_ATTRIBUTE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="42b7c-188">PRINTER_ATTRIBUTE_DEFAULT</span></span><br />
<span data-ttu-id="42b7c-189">PRINTER_ATTRIBUTE_SHARED</span><span class="sxs-lookup"><span data-stu-id="42b7c-189">PRINTER_ATTRIBUTE_SHARED</span></span><br />
</dl></td>
<td><span data-ttu-id="42b7c-190">0x0D</span><span class="sxs-lookup"><span data-stu-id="42b7c-190">0x0D</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-191">PRINTER_NOTIFY_FIELD_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="42b7c-191">PRINTER_NOTIFY_FIELD_PRIORITY</span></span></td>
<td><span data-ttu-id="42b7c-192"><strong>adwData</strong> [0] 指定多工緩衝處理器用來路由列印工作的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="42b7c-192"><strong>adwData</strong> [0] specifies a priority value that the spooler uses to route print jobs.</span></span></td>
<td><span data-ttu-id="42b7c-193">0x0E</span><span class="sxs-lookup"><span data-stu-id="42b7c-193">0x0E</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="42b7c-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span></span></td>
<td><span data-ttu-id="42b7c-195"><strong>adwData</strong> [0] 指定指派給每個列印工作的預設優先權值。</span><span class="sxs-lookup"><span data-stu-id="42b7c-195"><strong>adwData</strong> [0] specifies the default priority value assigned to each print job.</span></span></td>
<td><span data-ttu-id="42b7c-196">0x0F</span><span class="sxs-lookup"><span data-stu-id="42b7c-196">0x0F</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-197">PRINTER_NOTIFY_FIELD_START_TIME</span><span class="sxs-lookup"><span data-stu-id="42b7c-197">PRINTER_NOTIFY_FIELD_START_TIME</span></span></td>
<td><span data-ttu-id="42b7c-198"><strong>adwData</strong> [0] 指定印表機要列印工作的最早時間。</span><span class="sxs-lookup"><span data-stu-id="42b7c-198"><strong>adwData</strong> [0] specifies the earliest time at which the printer will print a job.</span></span> <span data-ttu-id="42b7c-199"> (此值指定的時間，在 12:00 A.M. 之後經過的時間 ) </span><span class="sxs-lookup"><span data-stu-id="42b7c-199">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="42b7c-200">0x10</span><span class="sxs-lookup"><span data-stu-id="42b7c-200">0x10</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span><span class="sxs-lookup"><span data-stu-id="42b7c-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span></span></td>
<td><span data-ttu-id="42b7c-202"><strong>adwData</strong> [0] 會指定印表機列印工作的最晚時間。</span><span class="sxs-lookup"><span data-stu-id="42b7c-202"><strong>adwData</strong> [0] specifies the latest time at which the printer will print a job.</span></span> <span data-ttu-id="42b7c-203"> (此值指定的時間，在 12:00 A.M. 之後經過的時間 ) </span><span class="sxs-lookup"><span data-stu-id="42b7c-203">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="42b7c-204">0x11</span><span class="sxs-lookup"><span data-stu-id="42b7c-204">0x11</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-205">PRINTER_NOTIFY_FIELD_STATUS</span><span class="sxs-lookup"><span data-stu-id="42b7c-205">PRINTER_NOTIFY_FIELD_STATUS</span></span></td>
<td><span data-ttu-id="42b7c-206"><strong>adwData</strong> [0] 指定印表機的狀態。</span><span class="sxs-lookup"><span data-stu-id="42b7c-206"><strong>adwData</strong> [0] specifies the printer status.</span></span> <span data-ttu-id="42b7c-207">如需可能值的清單，請參閱 <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="42b7c-207">For a list of possible values, see the <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> structure.</span></span></td>
<td><span data-ttu-id="42b7c-208">0x12</span><span class="sxs-lookup"><span data-stu-id="42b7c-208">0x12</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span><span class="sxs-lookup"><span data-stu-id="42b7c-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span></span></td>
<td><span data-ttu-id="42b7c-210">不支援。</span><span class="sxs-lookup"><span data-stu-id="42b7c-210">Not supported.</span></span></td>
<td><span data-ttu-id="42b7c-211">0x13</span><span class="sxs-lookup"><span data-stu-id="42b7c-211">0x13</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-212">PRINTER_NOTIFY_FIELD_CJOBS</span><span class="sxs-lookup"><span data-stu-id="42b7c-212">PRINTER_NOTIFY_FIELD_CJOBS</span></span></td>
<td><span data-ttu-id="42b7c-213"><strong>adwData</strong> [0] 指定印表機已排入佇列的列印工作數目。</span><span class="sxs-lookup"><span data-stu-id="42b7c-213"><strong>adwData</strong> [0] specifies the number of print jobs that have been queued for the printer.</span></span></td>
<td><span data-ttu-id="42b7c-214">0x14</span><span class="sxs-lookup"><span data-stu-id="42b7c-214">0x14</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span><span class="sxs-lookup"><span data-stu-id="42b7c-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span></span></td>
<td><span data-ttu-id="42b7c-216"><strong>adwData</strong> [0] 指定印表機上每分鐘列印的平均頁數。</span><span class="sxs-lookup"><span data-stu-id="42b7c-216"><strong>adwData</strong> [0] specifies the average number of pages per minute that have been printed on the printer.</span></span></td>
<td><span data-ttu-id="42b7c-217">0x15</span><span class="sxs-lookup"><span data-stu-id="42b7c-217">0x15</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span><span class="sxs-lookup"><span data-stu-id="42b7c-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span></span></td>
<td><span data-ttu-id="42b7c-219">不支援。</span><span class="sxs-lookup"><span data-stu-id="42b7c-219">Not supported.</span></span></td>
<td><span data-ttu-id="42b7c-220">0x16</span><span class="sxs-lookup"><span data-stu-id="42b7c-220">0x16</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="42b7c-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span></span></td>
<td><span data-ttu-id="42b7c-222">不支援。</span><span class="sxs-lookup"><span data-stu-id="42b7c-222">Not supported.</span></span></td>
<td><span data-ttu-id="42b7c-223">0x17</span><span class="sxs-lookup"><span data-stu-id="42b7c-223">0x17</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span><span class="sxs-lookup"><span data-stu-id="42b7c-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span></span></td>
<td><span data-ttu-id="42b7c-225">不支援。</span><span class="sxs-lookup"><span data-stu-id="42b7c-225">Not supported.</span></span></td>
<td><span data-ttu-id="42b7c-226">0x18</span><span class="sxs-lookup"><span data-stu-id="42b7c-226">0x18</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="42b7c-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span></span></td>
<td><span data-ttu-id="42b7c-228">不支援。</span><span class="sxs-lookup"><span data-stu-id="42b7c-228">Not supported.</span></span></td>
<td><span data-ttu-id="42b7c-229">0x19</span><span class="sxs-lookup"><span data-stu-id="42b7c-229">0x19</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42b7c-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span><span class="sxs-lookup"><span data-stu-id="42b7c-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span></span></td>
<td><span data-ttu-id="42b7c-231">這是在物件 GUID 變更時設定。</span><span class="sxs-lookup"><span data-stu-id="42b7c-231">This is set if the object GUID changes.</span></span></td>
<td><span data-ttu-id="42b7c-232">0x1A</span><span class="sxs-lookup"><span data-stu-id="42b7c-232">0x1A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42b7c-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="42b7c-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span></span></td>
<td><span data-ttu-id="42b7c-234">如果印表機連接已重新命名，就會設定此設定。</span><span class="sxs-lookup"><span data-stu-id="42b7c-234">This is set if the printer connection is renamed.</span></span></td>
<td><span data-ttu-id="42b7c-235">0x1B</span><span class="sxs-lookup"><span data-stu-id="42b7c-235">0x1B</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="42b7c-236">如果 **類型** 成員指定了工作 \_ 通知 \_ 類型， **欄位** 成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42b7c-236">If the **Type** member specifies JOB\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



| <span data-ttu-id="42b7c-237">欄位</span><span class="sxs-lookup"><span data-stu-id="42b7c-237">Field</span></span>                                    | <span data-ttu-id="42b7c-238">資料類型</span><span class="sxs-lookup"><span data-stu-id="42b7c-238">Type of data</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="42b7c-239">值</span><span class="sxs-lookup"><span data-stu-id="42b7c-239">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="42b7c-240">作業 \_ 通知 \_ 欄位 \_ 印表機 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="42b7c-240">JOB\_NOTIFY\_FIELD\_PRINTER\_NAME</span></span>        | <span data-ttu-id="42b7c-241">**pBuf** 是以 null 結束的字串指標，其中包含工作要進行多工緩衝處理的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-241">**pBuf** is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</span></span>                                                                                                                                      | <span data-ttu-id="42b7c-242">0x00</span><span class="sxs-lookup"><span data-stu-id="42b7c-242">0x00</span></span>  |
| <span data-ttu-id="42b7c-243">作業 \_ 通知 \_ 欄位 \_ 電腦 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="42b7c-243">JOB\_NOTIFY\_FIELD\_MACHINE\_NAME</span></span>        | <span data-ttu-id="42b7c-244">**pBuf** 是以 null 結束的字串指標，可指定建立列印工作的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-244">**pBuf** is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>                                                                                                                                    | <span data-ttu-id="42b7c-245">0x01</span><span class="sxs-lookup"><span data-stu-id="42b7c-245">0x01</span></span>  |
| <span data-ttu-id="42b7c-246">作業 \_ 通知 \_ 欄位 \_ 埠 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="42b7c-246">JOB\_NOTIFY\_FIELD\_PORT\_NAME</span></span>           | <span data-ttu-id="42b7c-247">**pBuf** 是以 null 結束的字串指標，可識別用來將資料傳輸至印表機的埠 (s) 。</span><span class="sxs-lookup"><span data-stu-id="42b7c-247">**pBuf** is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="42b7c-248">如果印表機連線到一個以上的埠，埠的名稱會以逗號分隔 (例如，"LPT1：，LPT2：，LPT3：" ) 。</span><span class="sxs-lookup"><span data-stu-id="42b7c-248">If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span> | <span data-ttu-id="42b7c-249">0x02</span><span class="sxs-lookup"><span data-stu-id="42b7c-249">0x02</span></span>  |
| <span data-ttu-id="42b7c-250">作業 \_ 通知 \_ 欄位 \_ 使用者 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="42b7c-250">JOB\_NOTIFY\_FIELD\_USER\_NAME</span></span>           | <span data-ttu-id="42b7c-251">**pBuf** 是以 null 結束的字串指標，可指定傳送列印工作之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-251">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</span></span>                                                                                                                                           | <span data-ttu-id="42b7c-252">0x03</span><span class="sxs-lookup"><span data-stu-id="42b7c-252">0x03</span></span>  |
| <span data-ttu-id="42b7c-253">作業 \_ 通知 \_ 欄位 \_ 通知 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="42b7c-253">JOB\_NOTIFY\_FIELD\_NOTIFY\_NAME</span></span>         | <span data-ttu-id="42b7c-254">**pBuf** 是以 null 結束的字串指標，可指定在列印工作或列印工作時發生錯誤時應通知的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-254">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>                                                              | <span data-ttu-id="42b7c-255">0x04</span><span class="sxs-lookup"><span data-stu-id="42b7c-255">0x04</span></span>  |
| <span data-ttu-id="42b7c-256">作業 \_ 通知 \_ 欄位 \_ 資料類型</span><span class="sxs-lookup"><span data-stu-id="42b7c-256">JOB\_NOTIFY\_FIELD\_DATATYPE</span></span>             | <span data-ttu-id="42b7c-257">**pBuf** 是以 null 結束的字串指標，可指定用來記錄列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="42b7c-257">**pBuf** is a pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>                                                                                                                                         | <span data-ttu-id="42b7c-258">0x05</span><span class="sxs-lookup"><span data-stu-id="42b7c-258">0x05</span></span>  |
| <span data-ttu-id="42b7c-259">作業 \_ 通知 \_ 欄位 \_ 列印 \_ 處理器</span><span class="sxs-lookup"><span data-stu-id="42b7c-259">JOB\_NOTIFY\_FIELD\_PRINT\_PROCESSOR</span></span>     | <span data-ttu-id="42b7c-260">**pBuf** 是以 null 結束的字串指標，可指定用來列印工作的列印處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-260">**pBuf** is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</span></span>                                                                                                                           | <span data-ttu-id="42b7c-261">0x06</span><span class="sxs-lookup"><span data-stu-id="42b7c-261">0x06</span></span>  |
| <span data-ttu-id="42b7c-262">作業 \_ 通知 \_ 欄位 \_ 參數</span><span class="sxs-lookup"><span data-stu-id="42b7c-262">JOB\_NOTIFY\_FIELD\_PARAMETERS</span></span>           | <span data-ttu-id="42b7c-263">**pBuf** 是以 null 結束的字串指標，可指定列印處理器參數。</span><span class="sxs-lookup"><span data-stu-id="42b7c-263">**pBuf** is a pointer to a null-terminated string that specifies print-processor parameters.</span></span>                                                                                                                                                            | <span data-ttu-id="42b7c-264">0x07</span><span class="sxs-lookup"><span data-stu-id="42b7c-264">0x07</span></span>  |
| <span data-ttu-id="42b7c-265">作業 \_ 通知 \_ 欄位 \_ 驅動程式 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="42b7c-265">JOB\_NOTIFY\_FIELD\_DRIVER\_NAME</span></span>         | <span data-ttu-id="42b7c-266">**pBuf** 是以 null 結束的字串指標，可指定應該用來處理列印工作的印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="42b7c-266">**pBuf** is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>                                                                                                           | <span data-ttu-id="42b7c-267">0x08</span><span class="sxs-lookup"><span data-stu-id="42b7c-267">0x08</span></span>  |
| <span data-ttu-id="42b7c-268">作業 \_ 通知 \_ 欄位 \_ DEVMODE</span><span class="sxs-lookup"><span data-stu-id="42b7c-268">JOB\_NOTIFY\_FIELD\_DEVMODE</span></span>              | <span data-ttu-id="42b7c-269">**pBuf** 是 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構的指標，其中包含印表機驅動程式的裝置初始化和環境資料。</span><span class="sxs-lookup"><span data-stu-id="42b7c-269">**pBuf** is a pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>                                                                                                        | <span data-ttu-id="42b7c-270">0x09</span><span class="sxs-lookup"><span data-stu-id="42b7c-270">0x09</span></span>  |
| <span data-ttu-id="42b7c-271">作業 \_ 通知 \_ 欄位 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="42b7c-271">JOB\_NOTIFY\_FIELD\_STATUS</span></span>               | <span data-ttu-id="42b7c-272">**adwData** \[0 \] 指定工作狀態。</span><span class="sxs-lookup"><span data-stu-id="42b7c-272">**adwData** \[0\] specifies the job status.</span></span> <span data-ttu-id="42b7c-273">如需可能值的清單，請參閱 [**作業 \_ 資訊 \_ 2**](job-info-2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="42b7c-273">For a list of possible values, see the [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>                                                                                                                        | <span data-ttu-id="42b7c-274">0x0A</span><span class="sxs-lookup"><span data-stu-id="42b7c-274">0x0A</span></span>  |
| <span data-ttu-id="42b7c-275">作業 \_ 通知 \_ 欄位 \_ 狀態 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="42b7c-275">JOB\_NOTIFY\_FIELD\_STATUS\_STRING</span></span>       | <span data-ttu-id="42b7c-276">**pBuf** 是以 null 結束的字串指標，可指定列印工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="42b7c-276">**pBuf** is a pointer to a null-terminated string that specifies the status of the print job.</span></span>                                                                                                                                                           | <span data-ttu-id="42b7c-277">0x0B</span><span class="sxs-lookup"><span data-stu-id="42b7c-277">0x0B</span></span>  |
| <span data-ttu-id="42b7c-278">作業 \_ 通知 \_ 欄位 \_ 安全 \_ 描述項</span><span class="sxs-lookup"><span data-stu-id="42b7c-278">JOB\_NOTIFY\_FIELD\_SECURITY\_DESCRIPTOR</span></span> | <span data-ttu-id="42b7c-279">不支援。</span><span class="sxs-lookup"><span data-stu-id="42b7c-279">Not supported.</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="42b7c-280">0x0C</span><span class="sxs-lookup"><span data-stu-id="42b7c-280">0x0C</span></span>  |
| <span data-ttu-id="42b7c-281">作業 \_ 通知 \_ 欄位 \_ 檔</span><span class="sxs-lookup"><span data-stu-id="42b7c-281">JOB\_NOTIFY\_FIELD\_DOCUMENT</span></span>             | <span data-ttu-id="42b7c-282">**pBuf** 是以 null 結束的字串指標，可指定列印工作的名稱 (例如 "ms-chap： Review.doc" ) 。</span><span class="sxs-lookup"><span data-stu-id="42b7c-282">**pBuf** is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>                                                                                                                        | <span data-ttu-id="42b7c-283">0x0D</span><span class="sxs-lookup"><span data-stu-id="42b7c-283">0x0D</span></span>  |
| <span data-ttu-id="42b7c-284">作業 \_ 通知 \_ 欄位 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="42b7c-284">JOB\_NOTIFY\_FIELD\_PRIORITY</span></span>             | <span data-ttu-id="42b7c-285">**adwData** \[0 \] 指定作業優先權。</span><span class="sxs-lookup"><span data-stu-id="42b7c-285">**adwData** \[0\] specifies the job priority.</span></span>                                                                                                                                                                                                           | <span data-ttu-id="42b7c-286">0x0E</span><span class="sxs-lookup"><span data-stu-id="42b7c-286">0x0E</span></span>  |
| <span data-ttu-id="42b7c-287">作業 \_ 通知 \_ 欄位 \_ 位置</span><span class="sxs-lookup"><span data-stu-id="42b7c-287">JOB\_NOTIFY\_FIELD\_POSITION</span></span>             | <span data-ttu-id="42b7c-288">**adwData** \[0 \] 指定工作在列印佇列中的位置。</span><span class="sxs-lookup"><span data-stu-id="42b7c-288">**adwData** \[0\] specifies the job's position in the print queue.</span></span>                                                                                                                                                                                      | <span data-ttu-id="42b7c-289">0x0F</span><span class="sxs-lookup"><span data-stu-id="42b7c-289">0x0F</span></span>  |
| <span data-ttu-id="42b7c-290">已 \_ 提交工作通知 \_ 欄位 \_</span><span class="sxs-lookup"><span data-stu-id="42b7c-290">JOB\_NOTIFY\_FIELD\_SUBMITTED</span></span>            | <span data-ttu-id="42b7c-291">**pBuf** 是 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構的指標，可指定提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="42b7c-291">**pBuf** is a pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>                                                                                                                          | <span data-ttu-id="42b7c-292">0x10</span><span class="sxs-lookup"><span data-stu-id="42b7c-292">0x10</span></span>  |
| <span data-ttu-id="42b7c-293">作業 \_ 通知 \_ 欄位 \_ 開始 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="42b7c-293">JOB\_NOTIFY\_FIELD\_START\_TIME</span></span>          | <span data-ttu-id="42b7c-294">**adwData** \[0 \] 指定可列印工作的最早時間。</span><span class="sxs-lookup"><span data-stu-id="42b7c-294">**adwData** \[0\] specifies the earliest time that the job can be printed.</span></span> <span data-ttu-id="42b7c-295"> (此值指定的時間，在 12:00 A.M. 之後經過的時間 ) </span><span class="sxs-lookup"><span data-stu-id="42b7c-295">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                | <span data-ttu-id="42b7c-296">0x11</span><span class="sxs-lookup"><span data-stu-id="42b7c-296">0x11</span></span>  |
| <span data-ttu-id="42b7c-297">作業 \_ 通知 \_ 欄位 \_ 至 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="42b7c-297">JOB\_NOTIFY\_FIELD\_UNTIL\_TIME</span></span>          | <span data-ttu-id="42b7c-298">**adwData** \[0 \] 指定可列印工作的最晚時間。</span><span class="sxs-lookup"><span data-stu-id="42b7c-298">**adwData** \[0\] specifies the latest time that the job can be printed.</span></span> <span data-ttu-id="42b7c-299"> (此值指定的時間，在 12:00 A.M. 之後經過的時間 ) </span><span class="sxs-lookup"><span data-stu-id="42b7c-299">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                  | <span data-ttu-id="42b7c-300">0x12</span><span class="sxs-lookup"><span data-stu-id="42b7c-300">0x12</span></span>  |
| <span data-ttu-id="42b7c-301">作業 \_ 通知 \_ 欄位 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="42b7c-301">JOB\_NOTIFY\_FIELD\_TIME</span></span>                 | <span data-ttu-id="42b7c-302">**adwData** \[0 \] 指定自作業開始列印以來經過的總時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="42b7c-302">**adwData** \[0\] specifies the total time, in seconds, that has elapsed since the job began printing.</span></span>                                                                                                                                                  | <span data-ttu-id="42b7c-303">0x13</span><span class="sxs-lookup"><span data-stu-id="42b7c-303">0x13</span></span>  |
| <span data-ttu-id="42b7c-304">作業 \_ 通知 \_ 欄位 \_ 總計 \_ 頁面</span><span class="sxs-lookup"><span data-stu-id="42b7c-304">JOB\_NOTIFY\_FIELD\_TOTAL\_PAGES</span></span>         | <span data-ttu-id="42b7c-305">**adwData** \[0 \] 指定作業的大小（以頁面為限）。</span><span class="sxs-lookup"><span data-stu-id="42b7c-305">**adwData** \[0\] specifies the size, in pages, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="42b7c-306">0x14</span><span class="sxs-lookup"><span data-stu-id="42b7c-306">0x14</span></span>  |
| <span data-ttu-id="42b7c-307">列印的工作 \_ 通知 \_ 欄位 \_ 頁面 \_</span><span class="sxs-lookup"><span data-stu-id="42b7c-307">JOB\_NOTIFY\_FIELD\_PAGES\_PRINTED</span></span>       | <span data-ttu-id="42b7c-308">**adwData** \[0 \] 指定已列印的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="42b7c-308">**adwData** \[0\] specifies the number of pages that have printed.</span></span>                                                                                                                                                                                      | <span data-ttu-id="42b7c-309">0x15</span><span class="sxs-lookup"><span data-stu-id="42b7c-309">0x15</span></span>  |
| <span data-ttu-id="42b7c-310">作業 \_ 通知 \_ 欄位 \_ 總 \_ 位元組數</span><span class="sxs-lookup"><span data-stu-id="42b7c-310">JOB\_NOTIFY\_FIELD\_TOTAL\_BYTES</span></span>         | <span data-ttu-id="42b7c-311">**adwData** \[0 \] 指定作業的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="42b7c-311">**adwData** \[0\] specifies the size, in bytes, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="42b7c-312">0x16</span><span class="sxs-lookup"><span data-stu-id="42b7c-312">0x16</span></span>  |
| <span data-ttu-id="42b7c-313">已 \_ 列印工作通知 \_ 欄位 \_ 位元組 \_</span><span class="sxs-lookup"><span data-stu-id="42b7c-313">JOB\_NOTIFY\_FIELD\_BYTES\_PRINTED</span></span>       | <span data-ttu-id="42b7c-314">**adwData** \[0 \] 指定在此作業上列印的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="42b7c-314">**adwData** \[0\] specifies the number of bytes that have been printed on this job.</span></span> <span data-ttu-id="42b7c-315">針對此欄位，當傳送位元組至印表機時，變更通知物件會收到信號。</span><span class="sxs-lookup"><span data-stu-id="42b7c-315">For this field, the change notification object is signaled when bytes are sent to the printer.</span></span>                                                                      | <span data-ttu-id="42b7c-316">0x17</span><span class="sxs-lookup"><span data-stu-id="42b7c-316">0x17</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="42b7c-317">規格需求</span><span class="sxs-lookup"><span data-stu-id="42b7c-317">Requirements</span></span>



| <span data-ttu-id="42b7c-318">需求</span><span class="sxs-lookup"><span data-stu-id="42b7c-318">Requirement</span></span> | <span data-ttu-id="42b7c-319">值</span><span class="sxs-lookup"><span data-stu-id="42b7c-319">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b7c-320">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42b7c-320">Minimum supported client</span></span><br/> | <span data-ttu-id="42b7c-321">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42b7c-321">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="42b7c-322">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42b7c-322">Minimum supported server</span></span><br/> | <span data-ttu-id="42b7c-323">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42b7c-323">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="42b7c-324">標頭</span><span class="sxs-lookup"><span data-stu-id="42b7c-324">Header</span></span><br/>                   | <dl> <span data-ttu-id="42b7c-325"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="42b7c-325"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42b7c-326">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42b7c-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b7c-327">列印</span><span class="sxs-lookup"><span data-stu-id="42b7c-327">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="42b7c-328">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="42b7c-328">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="42b7c-329">**版**</span><span class="sxs-lookup"><span data-stu-id="42b7c-329">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="42b7c-330">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="42b7c-330">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="42b7c-331">**作業 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="42b7c-331">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="42b7c-332">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="42b7c-332">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="42b7c-333">**印表機 \_ 通知 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="42b7c-333">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="42b7c-334">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="42b7c-334">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="42b7c-335">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="42b7c-335">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

