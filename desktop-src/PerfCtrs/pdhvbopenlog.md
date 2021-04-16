---
description: PdhVbOpenLog 函式會開啟指定的記錄檔以供讀取和寫入。 此函數會呼叫 PdhOpenLog。
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: PdhVbOpenLog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513404"
---
# <a name="pdhvbopenlog-function"></a><span data-ttu-id="dcf5b-104">PdhVbOpenLog 函式</span><span class="sxs-lookup"><span data-stu-id="dcf5b-104">PdhVbOpenLog function</span></span>

<span data-ttu-id="dcf5b-105">**PdhVbOpenLog** 函式會開啟指定的記錄檔以供讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-105">The **PdhVbOpenLog** function opens the specified log file for reading and writing.</span></span> <span data-ttu-id="dcf5b-106">此函數會呼叫 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-106">This function calls [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf5b-107">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="dcf5b-108">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="dcf5b-109">Function PdhVbOpenLog ( \_ Byval SzLogFileName AS LPCTSTR， \_ Byval DWACCESSFLAGS as dword，Byval \_ lpdwLogType as LPDWORD，BYVAL hQuery as \_ pdh \_ hQuery，byval dwMaxSize \_ \_ \_ \_ as，byval \_ szUserCaption as，BYREF LPCSTR as，) ByRef phLog 做為 dword</span><span class="sxs-lookup"><span data-stu-id="dcf5b-109">Function PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH\_HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH\_HLOG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="dcf5b-110">參數</span><span class="sxs-lookup"><span data-stu-id="dcf5b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf5b-111">*szLogFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-111">*szLogFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5b-112">字串的指標，指定要開啟之記錄檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-112">Pointer to a string that specifies the name of the log file to be opened.</span></span>

<span data-ttu-id="dcf5b-113">如果記錄檔包含 SQL 資料，則記錄檔名稱的格式為 **sql：** 資料包 *_！_*_LogFileName_。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-113">If the log file contains SQL data, the format of the name of the log file is **SQL:**_DataSourceName_*_!_*_LogFileName_.</span></span> <span data-ttu-id="dcf5b-114">在此情況下， *lpdwLogType* 參數的值為 PDH \_ 記錄 \_ 類型 \_ SQL。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-114">In this case, the value of the *lpdwLogType* parameter is PDH\_LOG\_TYPE\_SQL.</span></span>

</dd> <dt>

<span data-ttu-id="dcf5b-115">*dwAccessFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-115">*dwAccessFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5b-116">開啟記錄檔時所要指定的存取類型。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-116">Type of access to be specified when the log file is opened.</span></span> <span data-ttu-id="dcf5b-117">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="dcf5b-118">值</span><span class="sxs-lookup"><span data-stu-id="dcf5b-118">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="dcf5b-119">意義</span><span class="sxs-lookup"><span data-stu-id="dcf5b-119">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <span data-ttu-id="dcf5b-120"><dt>**PDH \_ 記錄 \_ 讀取 \_ 許可權**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-120"><dt>**PDH\_LOG\_READ\_ACCESS**</dt></span></span> </dl>       | <span data-ttu-id="dcf5b-121">開啟記錄檔以進行讀取作業。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-121">A log file is opened for a read operation.</span></span><br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <span data-ttu-id="dcf5b-122"><dt>**PDH \_ 記錄 \_ 寫入 \_ 許可權**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-122"><dt>**PDH\_LOG\_WRITE\_ACCESS**</dt></span></span> </dl>    | <span data-ttu-id="dcf5b-123">針對寫入作業開啟新的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-123">A new log file is opened for a write operation.</span></span><br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <span data-ttu-id="dcf5b-124"><dt>**PDH \_ 記錄 \_ 更新 \_ 存取**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-124"><dt>**PDH\_LOG\_UPDATE\_ACCESS**</dt></span></span> </dl> | <span data-ttu-id="dcf5b-125">針對寫入作業開啟現有的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-125">An existing log file is opened for a write operation.</span></span><br/> |



 

<span data-ttu-id="dcf5b-126">您可以使用 OR 運算子搭配下列其中一個 create access 旗標，來結合上表選取的值。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-126">The value selected from the previous table can be combined using the OR operator with one of the following create access flags.</span></span>



| <span data-ttu-id="dcf5b-127">值</span><span class="sxs-lookup"><span data-stu-id="dcf5b-127">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="dcf5b-128">意義</span><span class="sxs-lookup"><span data-stu-id="dcf5b-128">Meaning</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <span data-ttu-id="dcf5b-129"><dt>**PDH \_ 記錄 \_ 建立 \_ 新的**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-129"><dt>**PDH\_LOG\_CREATE\_NEW**</dt></span></span> </dl>          | <span data-ttu-id="dcf5b-130">建立具有指定名稱的新記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-130">A new log file with the specified name is created.</span></span><br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <span data-ttu-id="dcf5b-131"><dt>**PDH \_ 記錄 \_ \_ 一律建立**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-131"><dt>**PDH\_LOG\_CREATE\_ALWAYS**</dt></span></span> </dl> | <span data-ttu-id="dcf5b-132">將會建立具有指定名稱的新記錄檔，並且會清除具有相同名稱的任何現有記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-132">A new log file with the specified name is created and any existing log file with the same name is erased.</span></span><br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <span data-ttu-id="dcf5b-133"><dt>**PDH \_ 記錄 \_ 開啟 \_ 現有的**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-133"><dt>**PDH\_LOG\_OPEN\_EXISTING**</dt></span></span> </dl> | <span data-ttu-id="dcf5b-134">開啟具有指定之名稱的現有記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-134">An existing log file with the specified name is opened.</span></span> <span data-ttu-id="dcf5b-135">如果具有指定名稱的記錄檔不存在，這就等於 PDH \_ 記錄 \_ 新建 \_ 。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-135">If a log file with the specified name does not exist, this is equal to PDH\_LOG\_CREATE\_NEW.</span></span><br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <span data-ttu-id="dcf5b-136"><dt>**PDH \_ 記錄 \_ \_ 一律開啟**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-136"><dt>**PDH\_LOG\_OPEN\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="dcf5b-137">系統會開啟具有指定名稱的現有記錄檔，或建立具有指定名稱的新記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-137">An existing log file with the specified name is opened or a new log file with the specified name is created.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="dcf5b-138">*lpdwLogType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-138">*lpdwLogType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5b-139">變數的指標，指出要開啟的記錄檔類型。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-139">Pointer to a variable that indicates the type of log file to be opened.</span></span> <span data-ttu-id="dcf5b-140">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-140">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="dcf5b-141">值</span><span class="sxs-lookup"><span data-stu-id="dcf5b-141">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="dcf5b-142">意義</span><span class="sxs-lookup"><span data-stu-id="dcf5b-142">Meaning</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <span data-ttu-id="dcf5b-143"><dt>**PDH \_ 記錄 \_ 類型 \_ 未定義**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-143"><dt>**PDH\_LOG\_TYPE\_UNDEFINED**</dt></span></span> </dl> | <span data-ttu-id="dcf5b-144">未定義的記錄檔格式。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-144">Undefined log file format.</span></span><br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <span data-ttu-id="dcf5b-145"><dt>**PDH \_ 記錄 \_ 類型 \_ CSV**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-145"><dt>**PDH\_LOG\_TYPE\_CSV**</dt></span></span> </dl>                   | <span data-ttu-id="dcf5b-146">在第一行包含資料行標頭的文字檔，以及每個後續行中的個別資料範例。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-146">Text files containing column headers in the first line, and individual data samples in each subsequent line.</span></span><br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <span data-ttu-id="dcf5b-147"><dt>**PDH \_ 記錄 \_ 類型 \_ SQL**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-147"><dt>**PDH\_LOG\_TYPE\_SQL**</dt></span></span> </dl>                   | <span data-ttu-id="dcf5b-148">記錄檔中的資料是在 SQL 中。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-148">The data in the log file is in SQL.</span></span><br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <span data-ttu-id="dcf5b-149"><dt>**PDH \_ 記錄 \_ 類型 \_ TSV**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-149"><dt>**PDH\_LOG\_TYPE\_TSV**</dt></span></span> </dl>                   | <span data-ttu-id="dcf5b-150">與 PDH \_ 記錄檔 \_ 類型 \_ CSV 相同。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-150">Same as PDH\_LOG\_TYPE\_CSV.</span></span><br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <span data-ttu-id="dcf5b-151"><dt>**PDH \_ 記錄 \_ 類型 \_ 二進位**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-151"><dt>**PDH\_LOG\_TYPE\_BINARY**</dt></span></span> </dl>          | <span data-ttu-id="dcf5b-152">二進位記錄檔格式。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-152">Binary log file format.</span></span> <span data-ttu-id="dcf5b-153">包含迴圈記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-153">Includes circular log files.</span></span><br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <span data-ttu-id="dcf5b-154"><dt>**PDH \_ 記錄 \_ 類型 \_ PERFMON**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-154"><dt>**PDH\_LOG\_TYPE\_PERFMON**</dt></span></span> </dl>       | <span data-ttu-id="dcf5b-155">Perfmon 記錄檔格式。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-155">Perfmon log file format.</span></span><br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="dcf5b-156">*hQuery* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-156">*hQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5b-157">查詢控制碼。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-157">Query handle.</span></span> <span data-ttu-id="dcf5b-158">[**PdhVbOpenQuery**](pdhvbopenquery.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-158">This handle is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

<span data-ttu-id="dcf5b-159">如果要開啟記錄檔以供讀取，這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-159">This parameter can be **NULL** if the log file is to be opened for reading.</span></span>

</dd> <dt>

<span data-ttu-id="dcf5b-160">*dwMaxSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-160">*dwMaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5b-161">記錄檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-161">Maximum size of the log file, in bytes.</span></span> <span data-ttu-id="dcf5b-162">只有當記錄檔是有限大小或迴圈的記錄檔時，才會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-162">This value is used only if the log file is a limited-size or circular log file.</span></span>

</dd> <dt>

<span data-ttu-id="dcf5b-163">*szUserCaption* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-163">*szUserCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5b-164">字串的指標，指定記錄檔的使用者定義標題。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-164">Pointer to a string that specifies the user-defined caption of the log file.</span></span> <span data-ttu-id="dcf5b-165">記錄檔標題通常會描述記錄檔的內容。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-165">A log file caption generally describes the contents of the log file.</span></span> <span data-ttu-id="dcf5b-166">開啟現有的記錄檔時，會忽略這個參數的值。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-166">When an existing log file is opened, the value of this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="dcf5b-167">*phLog* \[在中，ref\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-167">*phLog* \[in, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5b-168">接收已開啟記錄檔之控制碼的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-168">Pointer to a buffer that receives a handle to the opened log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf5b-169">傳回值</span><span class="sxs-lookup"><span data-stu-id="dcf5b-169">Return value</span></span>

<span data-ttu-id="dcf5b-170">如果函數成功，它會傳回0。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-170">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="dcf5b-171">如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-171">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="dcf5b-172">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-172">The following are possible values.</span></span>



| <span data-ttu-id="dcf5b-173">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dcf5b-173">Return code</span></span>                                                                                                | <span data-ttu-id="dcf5b-174">Description</span><span class="sxs-lookup"><span data-stu-id="dcf5b-174">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcf5b-175"><dt>**PDH \_ \_ 緩衝區不足**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-175"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="dcf5b-176">要求的資料大於提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-176">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="dcf5b-177">無法傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-177">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="dcf5b-178"><dt>**PDH \_ 不正確 \_ 引數**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-178"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="dcf5b-179">一或多個字串緩衝區的大小不正確。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-179">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="dcf5b-180"><dt>**PDH \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-180"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="dcf5b-181">控制碼不是有效的 PDH 物件。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-181">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="dcf5b-182"><dt>**PDH \_ 記錄 \_ 檔 \_ 開啟 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-182"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="dcf5b-183">無法開啟指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-183">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="dcf5b-184"><dt>**\_ \_ \_ 找不到 PDH 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-184"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="dcf5b-185">找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-185">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="dcf5b-186">備註</span><span class="sxs-lookup"><span data-stu-id="dcf5b-186">Remarks</span></span>

<span data-ttu-id="dcf5b-187">使用這個函數將效能資料寫入記錄檔時，必須先使用 [**PdhVbOpenQuery**](pdhvbopenquery.md)開啟查詢。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-187">When using this function to write performance data to a log file, a query must first be opened using [**PdhVbOpenQuery**](pdhvbopenquery.md).</span></span>

<span data-ttu-id="dcf5b-188">在呼叫此函式之前，必須要有目前開啟的查詢，而且必須將所需的計數器新增至其中。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-188">There must be a currently opened query, and the desired counters must be added to it, before this function is called.</span></span>

<span data-ttu-id="dcf5b-189">請注意，Perfmon 格式的記錄檔只能開啟以供讀取。</span><span class="sxs-lookup"><span data-stu-id="dcf5b-189">Note that log files in the Perfmon format can only be opened for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf5b-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcf5b-190">Requirements</span></span>



| <span data-ttu-id="dcf5b-191">需求</span><span class="sxs-lookup"><span data-stu-id="dcf5b-191">Requirement</span></span> | <span data-ttu-id="dcf5b-192">值</span><span class="sxs-lookup"><span data-stu-id="dcf5b-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf5b-193">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcf5b-193">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf5b-194">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-194">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcf5b-195">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcf5b-195">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf5b-196">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcf5b-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dcf5b-197">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcf5b-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcf5b-198"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-198"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="dcf5b-199">DLL</span><span class="sxs-lookup"><span data-stu-id="dcf5b-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcf5b-200"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5b-200"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf5b-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcf5b-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf5b-202">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="dcf5b-202">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[<span data-ttu-id="dcf5b-203">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="dcf5b-203">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="dcf5b-204">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="dcf5b-204">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

