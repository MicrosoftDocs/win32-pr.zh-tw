---
description: SummaryInfo 物件的 Property 屬性會設定或取得摘要資訊資料流程中指定之屬性的值。
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994672"
---
# <a name="summaryinfoproperty-property"></a><span data-ttu-id="2cf15-103">SummaryInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="2cf15-103">SummaryInfo.Property property</span></span>

<span data-ttu-id="2cf15-104">[**SummaryInfo**](summaryinfo-object.md)物件的 **property** 屬性會設定或取得摘要資訊資料流程中指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2cf15-104">The **Property** property of the [**SummaryInfo**](summaryinfo-object.md) object sets or gets the value for the specified property in the summary information stream.</span></span> <span data-ttu-id="2cf15-105">建立 [**SummaryInfo**](summaryinfo-object.md) 物件時，會讀取屬性，但是在呼叫 [**保存**](summaryinfo-persist.md) 方法之前，都不會寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="2cf15-105">The properties are read when the [**SummaryInfo**](summaryinfo-object.md) object is created, but they are not written until the [**Persist**](summaryinfo-persist.md) method is called.</span></span> <span data-ttu-id="2cf15-106">將屬性設為空白會導致移除;同樣地，要求不存在的屬性會傳回空值。</span><span class="sxs-lookup"><span data-stu-id="2cf15-106">Setting a property to Empty causes its removal; likewise, requesting a nonexistent property returns an Empty value.</span></span> <span data-ttu-id="2cf15-107">否則，值可能會以字串、整數或日期 (日期時間) 類型來傳送。</span><span class="sxs-lookup"><span data-stu-id="2cf15-107">Otherwise values may be transferred as strings, integers, or date (date time) types.</span></span>

<span data-ttu-id="2cf15-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2cf15-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf15-109">語法</span><span class="sxs-lookup"><span data-stu-id="2cf15-109">Syntax</span></span>


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a><span data-ttu-id="2cf15-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2cf15-110">Property value</span></span>

<span data-ttu-id="2cf15-111">其中一個摘要屬性的必要屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="2cf15-111">Required property ID of one of the summary properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf15-112">備註</span><span class="sxs-lookup"><span data-stu-id="2cf15-112">Remarks</span></span>

<span data-ttu-id="2cf15-113">**標準摘要屬性識別碼**</span><span class="sxs-lookup"><span data-stu-id="2cf15-113">**Standard Summary Property IDs**</span></span>

<span data-ttu-id="2cf15-114"> (不是列舉) </span><span class="sxs-lookup"><span data-stu-id="2cf15-114">(not an enumeration)</span></span>



| <span data-ttu-id="2cf15-115">參數名稱</span><span class="sxs-lookup"><span data-stu-id="2cf15-115">Parameter name</span></span>     | <span data-ttu-id="2cf15-116">值</span><span class="sxs-lookup"><span data-stu-id="2cf15-116">Value</span></span> | <span data-ttu-id="2cf15-117">描述</span><span class="sxs-lookup"><span data-stu-id="2cf15-117">Description</span></span>                                       |
|--------------------|-------|---------------------------------------------------|
| <span data-ttu-id="2cf15-118">PID \_ 字典</span><span class="sxs-lookup"><span data-stu-id="2cf15-118">PID\_DICTIONARY</span></span>    | <span data-ttu-id="2cf15-119">0</span><span class="sxs-lookup"><span data-stu-id="2cf15-119">0</span></span>     | <span data-ttu-id="2cf15-120">SummaryInfo 物件不支援的特殊格式</span><span class="sxs-lookup"><span data-stu-id="2cf15-120">Special format, not support by SummaryInfo object</span></span> |
| <span data-ttu-id="2cf15-121">PID \_ 字碼頁</span><span class="sxs-lookup"><span data-stu-id="2cf15-121">PID\_CODEPAGE</span></span>      | <span data-ttu-id="2cf15-122">1</span><span class="sxs-lookup"><span data-stu-id="2cf15-122">1</span></span>     | <span data-ttu-id="2cf15-123">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="2cf15-123">VT\_I2</span></span>                                            |
| <span data-ttu-id="2cf15-124">PID \_ 標題</span><span class="sxs-lookup"><span data-stu-id="2cf15-124">PID\_TITLE</span></span>         | <span data-ttu-id="2cf15-125">2</span><span class="sxs-lookup"><span data-stu-id="2cf15-125">2</span></span>     | <span data-ttu-id="2cf15-126">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-126">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-127">PID \_ 主體</span><span class="sxs-lookup"><span data-stu-id="2cf15-127">PID\_SUBJECT</span></span>       | <span data-ttu-id="2cf15-128">3</span><span class="sxs-lookup"><span data-stu-id="2cf15-128">3</span></span>     | <span data-ttu-id="2cf15-129">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-129">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-130">PID \_ 作者</span><span class="sxs-lookup"><span data-stu-id="2cf15-130">PID\_AUTHOR</span></span>        | <span data-ttu-id="2cf15-131">4</span><span class="sxs-lookup"><span data-stu-id="2cf15-131">4</span></span>     | <span data-ttu-id="2cf15-132">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-132">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-133">PID \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="2cf15-133">PID\_KEYWORDS</span></span>      | <span data-ttu-id="2cf15-134">5</span><span class="sxs-lookup"><span data-stu-id="2cf15-134">5</span></span>     | <span data-ttu-id="2cf15-135">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-135">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-136">PID \_ 批註</span><span class="sxs-lookup"><span data-stu-id="2cf15-136">PID\_COMMENTS</span></span>      | <span data-ttu-id="2cf15-137">6</span><span class="sxs-lookup"><span data-stu-id="2cf15-137">6</span></span>     | <span data-ttu-id="2cf15-138">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-138">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-139">PID \_ 範本</span><span class="sxs-lookup"><span data-stu-id="2cf15-139">PID\_TEMPLATE</span></span>      | <span data-ttu-id="2cf15-140">7</span><span class="sxs-lookup"><span data-stu-id="2cf15-140">7</span></span>     | <span data-ttu-id="2cf15-141">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-141">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-142">PID \_ LASTAUTHOR</span><span class="sxs-lookup"><span data-stu-id="2cf15-142">PID\_LASTAUTHOR</span></span>    | <span data-ttu-id="2cf15-143">8</span><span class="sxs-lookup"><span data-stu-id="2cf15-143">8</span></span>     | <span data-ttu-id="2cf15-144">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-144">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-145">PID \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="2cf15-145">PID\_REVNUMBER</span></span>     | <span data-ttu-id="2cf15-146">9</span><span class="sxs-lookup"><span data-stu-id="2cf15-146">9</span></span>     | <span data-ttu-id="2cf15-147">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-147">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-148">PID \_ EDITTIME</span><span class="sxs-lookup"><span data-stu-id="2cf15-148">PID\_EDITTIME</span></span>      | <span data-ttu-id="2cf15-149">10</span><span class="sxs-lookup"><span data-stu-id="2cf15-149">10</span></span>    | <span data-ttu-id="2cf15-150">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="2cf15-150">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="2cf15-151">PID \_ LASTPRINTED</span><span class="sxs-lookup"><span data-stu-id="2cf15-151">PID\_LASTPRINTED</span></span>   | <span data-ttu-id="2cf15-152">11</span><span class="sxs-lookup"><span data-stu-id="2cf15-152">11</span></span>    | <span data-ttu-id="2cf15-153">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="2cf15-153">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="2cf15-154">PID \_ 建立 \_ DTM</span><span class="sxs-lookup"><span data-stu-id="2cf15-154">PID\_CREATE\_DTM</span></span>   | <span data-ttu-id="2cf15-155">12</span><span class="sxs-lookup"><span data-stu-id="2cf15-155">12</span></span>    | <span data-ttu-id="2cf15-156">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="2cf15-156">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="2cf15-157">PID \_ LASTSAVE \_ DTM</span><span class="sxs-lookup"><span data-stu-id="2cf15-157">PID\_LASTSAVE\_DTM</span></span> | <span data-ttu-id="2cf15-158">13</span><span class="sxs-lookup"><span data-stu-id="2cf15-158">13</span></span>    | <span data-ttu-id="2cf15-159">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="2cf15-159">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="2cf15-160">PID \_ PAGECOUNT</span><span class="sxs-lookup"><span data-stu-id="2cf15-160">PID\_PAGECOUNT</span></span>     | <span data-ttu-id="2cf15-161">14</span><span class="sxs-lookup"><span data-stu-id="2cf15-161">14</span></span>    | <span data-ttu-id="2cf15-162">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2cf15-162">VT\_I4</span></span>                                            |
| <span data-ttu-id="2cf15-163">PID \_ WORDCOUNT</span><span class="sxs-lookup"><span data-stu-id="2cf15-163">PID\_WORDCOUNT</span></span>     | <span data-ttu-id="2cf15-164">15</span><span class="sxs-lookup"><span data-stu-id="2cf15-164">15</span></span>    | <span data-ttu-id="2cf15-165">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2cf15-165">VT\_I4</span></span>                                            |
| <span data-ttu-id="2cf15-166">PID \_ >CHARCOUNT</span><span class="sxs-lookup"><span data-stu-id="2cf15-166">PID\_CHARCOUNT</span></span>     | <span data-ttu-id="2cf15-167">16</span><span class="sxs-lookup"><span data-stu-id="2cf15-167">16</span></span>    | <span data-ttu-id="2cf15-168">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2cf15-168">VT\_I4</span></span>                                            |
| <span data-ttu-id="2cf15-169">PID \_ 縮圖</span><span class="sxs-lookup"><span data-stu-id="2cf15-169">PID\_THUMBNAIL</span></span>     | <span data-ttu-id="2cf15-170">17</span><span class="sxs-lookup"><span data-stu-id="2cf15-170">17</span></span>    | <span data-ttu-id="2cf15-171">\_不支援 VT CF () </span><span class="sxs-lookup"><span data-stu-id="2cf15-171">VT\_CF (not supported)</span></span>                            |
| <span data-ttu-id="2cf15-172">PID \_ APPNAME</span><span class="sxs-lookup"><span data-stu-id="2cf15-172">PID\_APPNAME</span></span>       | <span data-ttu-id="2cf15-173">18</span><span class="sxs-lookup"><span data-stu-id="2cf15-173">18</span></span>    | <span data-ttu-id="2cf15-174">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-174">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="2cf15-175">PID \_ 安全性</span><span class="sxs-lookup"><span data-stu-id="2cf15-175">PID\_SECURITY</span></span>      | <span data-ttu-id="2cf15-176">19</span><span class="sxs-lookup"><span data-stu-id="2cf15-176">19</span></span>    | <span data-ttu-id="2cf15-177">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2cf15-177">VT\_I4</span></span>                                            |



 

<span data-ttu-id="2cf15-178">**屬性資料類型**</span><span class="sxs-lookup"><span data-stu-id="2cf15-178">**Property Data Types**</span></span>

<span data-ttu-id="2cf15-179"> (不是列舉) </span><span class="sxs-lookup"><span data-stu-id="2cf15-179">(not an enumeration)</span></span>



| <span data-ttu-id="2cf15-180">參數名稱</span><span class="sxs-lookup"><span data-stu-id="2cf15-180">Parameter name</span></span> | <span data-ttu-id="2cf15-181">值</span><span class="sxs-lookup"><span data-stu-id="2cf15-181">Value</span></span> | <span data-ttu-id="2cf15-182">描述</span><span class="sxs-lookup"><span data-stu-id="2cf15-182">Description</span></span>                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf15-183">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="2cf15-183">VT\_I2</span></span>         | <span data-ttu-id="2cf15-184">2</span><span class="sxs-lookup"><span data-stu-id="2cf15-184">2</span></span>     | <span data-ttu-id="2cf15-185">16位整數</span><span class="sxs-lookup"><span data-stu-id="2cf15-185">16-bit integer</span></span>                                                                           |
| <span data-ttu-id="2cf15-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2cf15-186">VT\_I4</span></span>         | <span data-ttu-id="2cf15-187">3</span><span class="sxs-lookup"><span data-stu-id="2cf15-187">3</span></span>     | <span data-ttu-id="2cf15-188">32 位元整數</span><span class="sxs-lookup"><span data-stu-id="2cf15-188">32-bit integer</span></span>                                                                           |
| <span data-ttu-id="2cf15-189">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="2cf15-189">VT\_LPSTR</span></span>      | <span data-ttu-id="2cf15-190">30</span><span class="sxs-lookup"><span data-stu-id="2cf15-190">30</span></span>    | <span data-ttu-id="2cf15-191">String</span><span class="sxs-lookup"><span data-stu-id="2cf15-191">String</span></span>                                                                                   |
| <span data-ttu-id="2cf15-192">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="2cf15-192">VT\_FILETIME</span></span>   | <span data-ttu-id="2cf15-193">64</span><span class="sxs-lookup"><span data-stu-id="2cf15-193">64</span></span>    | <span data-ttu-id="2cf15-194">日期時間 (FILETIME，轉換成變異時間) </span><span class="sxs-lookup"><span data-stu-id="2cf15-194">Date time (FILETIME, converted to Variant time)</span></span>                                          |
| <span data-ttu-id="2cf15-195">VT \_ CF</span><span class="sxs-lookup"><span data-stu-id="2cf15-195">VT\_CF</span></span>         | <span data-ttu-id="2cf15-196">71</span><span class="sxs-lookup"><span data-stu-id="2cf15-196">71</span></span>    | <span data-ttu-id="2cf15-197">剪貼簿格式 + 資料，不是由 [**SummaryInfo**](summaryinfo-object.md) 物件處理</span><span class="sxs-lookup"><span data-stu-id="2cf15-197">Clipboard format + data, not handled by [**SummaryInfo**](summaryinfo-object.md) object</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2cf15-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cf15-198">Requirements</span></span>



| <span data-ttu-id="2cf15-199">需求</span><span class="sxs-lookup"><span data-stu-id="2cf15-199">Requirement</span></span> | <span data-ttu-id="2cf15-200">值</span><span class="sxs-lookup"><span data-stu-id="2cf15-200">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf15-201">版本</span><span class="sxs-lookup"><span data-stu-id="2cf15-201">Version</span></span><br/> | <span data-ttu-id="2cf15-202">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="2cf15-202">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2cf15-203">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="2cf15-203">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2cf15-204">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2cf15-204">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2cf15-205">DLL</span><span class="sxs-lookup"><span data-stu-id="2cf15-205">DLL</span></span><br/>     | <dl> <span data-ttu-id="2cf15-206"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cf15-206"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2cf15-207">IID</span><span class="sxs-lookup"><span data-stu-id="2cf15-207">IID</span></span><br/>     | <span data-ttu-id="2cf15-208">IID \_ ISummaryInfo 定義為 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2cf15-208">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="2cf15-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cf15-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf15-210">**MsiSummaryInfoSetProperty**</span><span class="sxs-lookup"><span data-stu-id="2cf15-210">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[<span data-ttu-id="2cf15-211">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="2cf15-211">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




