---
description: 從屬於 EXE 專案的指定專案中抓取資料。
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385864"
---
# <a name="sdbquerydataextagid-function"></a><span data-ttu-id="58aa4-103">SdbQueryDataExTagID 函式</span><span class="sxs-lookup"><span data-stu-id="58aa4-103">SdbQueryDataExTagID function</span></span>

<span data-ttu-id="58aa4-104">從屬於 EXE 專案的指定專案中抓取資料。</span><span class="sxs-lookup"><span data-stu-id="58aa4-104">Retrieves data from the specified entries belonging to an EXE entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="58aa4-105">語法</span><span class="sxs-lookup"><span data-stu-id="58aa4-105">Syntax</span></span>


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a><span data-ttu-id="58aa4-106">參數</span><span class="sxs-lookup"><span data-stu-id="58aa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58aa4-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58aa4-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="58aa4-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="58aa4-109">*tiExe* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-109">*tiExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58aa4-110">EXE 專案的 [**TAGID**](tagid.md) 。</span><span class="sxs-lookup"><span data-stu-id="58aa4-110">The [**TAGID**](tagid.md) of the EXE entry.</span></span>

</dd> <dt>

<span data-ttu-id="58aa4-111">*lpszDataName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-111">*lpszDataName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58aa4-112">要抓取的資料輸入名稱。</span><span class="sxs-lookup"><span data-stu-id="58aa4-112">The name of the data entry to be retrieved.</span></span> <span data-ttu-id="58aa4-113">若要指定多個專案，請以反斜線字元分隔名稱 ( " \\ " ) 。</span><span class="sxs-lookup"><span data-stu-id="58aa4-113">To specify multiple entries, separate the names with the backslash character ("\\").</span></span> <span data-ttu-id="58aa4-114">如果此參數為 **Null**，則函式會嘗試傳回所有資料項目。</span><span class="sxs-lookup"><span data-stu-id="58aa4-114">If this parameter is **NULL**, the function attempts to return all data entries.</span></span>

</dd> <dt>

<span data-ttu-id="58aa4-115">*lpdwDataType* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-115">*lpdwDataType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58aa4-116">傳回之專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="58aa4-116">The data type of the returned entries.</span></span> <span data-ttu-id="58aa4-117">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="58aa4-117">This parameter can be one of the following values:</span></span>

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

<span data-ttu-id="58aa4-118">**REG \_ 二進位檔**</span><span class="sxs-lookup"><span data-stu-id="58aa4-118">**REG\_BINARY**</span></span>
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

<span data-ttu-id="58aa4-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="58aa4-119">**REG\_DWORD**</span></span>
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

<span data-ttu-id="58aa4-120">**REG \_ 多重 \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="58aa4-120">**REG\_MULTI\_SZ**</span></span>
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

<span data-ttu-id="58aa4-121">**REG \_ 無**</span><span class="sxs-lookup"><span data-stu-id="58aa4-121">**REG\_NONE**</span></span>
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

<span data-ttu-id="58aa4-122">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="58aa4-122">**REG\_QWORD**</span></span>
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

<span data-ttu-id="58aa4-123">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="58aa4-123">**REG\_SZ**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="58aa4-124">*lpBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-124">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58aa4-125">接收資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="58aa4-125">The buffer that receives the data.</span></span> <span data-ttu-id="58aa4-126">如果緩衝區不夠大，無法包含資料，則函數會失敗，並傳回 **錯誤 \_ 的 \_ 緩衝區**。</span><span class="sxs-lookup"><span data-stu-id="58aa4-126">If buffer is not large enough to contain the data, the function fails and returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span>

</dd> <dt>

<span data-ttu-id="58aa4-127">*lpcbBufferSize* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-127">*lpcbBufferSize* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58aa4-128">*LpBuffer* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="58aa4-128">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="58aa4-129">*ptiData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-129">*ptiData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58aa4-130">資料輸入的 [**TAGID**](tagid.md) 。</span><span class="sxs-lookup"><span data-stu-id="58aa4-130">The [**TAGID**](tagid.md) of the data entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58aa4-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="58aa4-131">Return value</span></span>

<span data-ttu-id="58aa4-132">此函數會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="58aa4-132">This function returns one of the following values.</span></span>



| <span data-ttu-id="58aa4-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="58aa4-133">Return code</span></span>                                                                                                    | <span data-ttu-id="58aa4-134">Description</span><span class="sxs-lookup"><span data-stu-id="58aa4-134">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58aa4-135"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="58aa4-135"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>       | <span data-ttu-id="58aa4-136">一或多個輸入參數不正確。</span><span class="sxs-lookup"><span data-stu-id="58aa4-136">One or more input parameters is incorrect.</span></span><br/>                  |
| <dl> <span data-ttu-id="58aa4-137"><dt>**\_內部 \_ 資料庫 \_ 損毀錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="58aa4-137"><dt>**ERROR\_INTERNAL\_DB\_CORRUPTION**</dt></span></span> </dl> | <span data-ttu-id="58aa4-138">找不到 EXE 專案的資料項目目。</span><span class="sxs-lookup"><span data-stu-id="58aa4-138">No data entries were found for the EXE entry.</span></span><br/>               |
| <dl> <span data-ttu-id="58aa4-139"><dt>**\_緩衝區不足的錯誤 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58aa4-139"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>     | <span data-ttu-id="58aa4-140">緩衝區不夠大，無法包含資料項目目。</span><span class="sxs-lookup"><span data-stu-id="58aa4-140">The buffer is not large enough to contain the data entries.</span></span><br/> |
| <dl> <span data-ttu-id="58aa4-141"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="58aa4-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>      | <span data-ttu-id="58aa4-142">記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="58aa4-142">The memory allocation failed.</span></span><br/>                               |
| <dl> <span data-ttu-id="58aa4-143"><dt>**\_找不 \_ 到錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="58aa4-143"><dt>**ERROR\_NOT\_FOUND**</dt></span></span> </dl>               | <span data-ttu-id="58aa4-144">找不到名稱為 *lpszDataName* 的資料輸入。</span><span class="sxs-lookup"><span data-stu-id="58aa4-144">A data entry with the name *lpszDataName* was not found.</span></span><br/>    |
| <dl> <span data-ttu-id="58aa4-145"><dt>**錯誤 \_ 成功**</dt></span><span class="sxs-lookup"><span data-stu-id="58aa4-145"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>                  | <span data-ttu-id="58aa4-146">函數已順利完成。</span><span class="sxs-lookup"><span data-stu-id="58aa4-146">The function completed successfully.</span></span><br/>                        |



 

## <a name="requirements"></a><span data-ttu-id="58aa4-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="58aa4-147">Requirements</span></span>



| <span data-ttu-id="58aa4-148">需求</span><span class="sxs-lookup"><span data-stu-id="58aa4-148">Requirement</span></span> | <span data-ttu-id="58aa4-149">值</span><span class="sxs-lookup"><span data-stu-id="58aa4-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58aa4-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58aa4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="58aa4-151">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-151">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="58aa4-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58aa4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="58aa4-153">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58aa4-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="58aa4-154">DLL</span><span class="sxs-lookup"><span data-stu-id="58aa4-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58aa4-155"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58aa4-155"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




