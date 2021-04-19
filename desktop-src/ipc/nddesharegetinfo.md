---
description: 捕獲 DDE 共用資訊。 這通常是為了編輯而完成。
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: 'NDdeShareGetInfo 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966663"
---
# <a name="nddesharegetinfo-function"></a><span data-ttu-id="100b8-104">NDdeShareGetInfo 函式</span><span class="sxs-lookup"><span data-stu-id="100b8-104">NDdeShareGetInfo function</span></span>

<span data-ttu-id="100b8-105">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="100b8-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="100b8-106">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="100b8-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="100b8-107">捕獲 DDE 共用資訊。</span><span class="sxs-lookup"><span data-stu-id="100b8-107">Retrieves DDE share information.</span></span> <span data-ttu-id="100b8-108">這通常是為了編輯而完成。</span><span class="sxs-lookup"><span data-stu-id="100b8-108">This is usually done for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="100b8-109">語法</span><span class="sxs-lookup"><span data-stu-id="100b8-109">Syntax</span></span>


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a><span data-ttu-id="100b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="100b8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="100b8-111">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="100b8-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100b8-112">DSDM 所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="100b8-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="100b8-113">*lpszShareName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="100b8-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100b8-114">要從 DSDM 中取出其資訊的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="100b8-114">The share name whose information is to be retrieved from the DSDM.</span></span> <span data-ttu-id="100b8-115">此參數不得為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="100b8-115">This parameter must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="100b8-116">*nLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="100b8-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100b8-117">資訊層級。</span><span class="sxs-lookup"><span data-stu-id="100b8-117">The information level.</span></span> <span data-ttu-id="100b8-118">此參數必須是2。</span><span class="sxs-lookup"><span data-stu-id="100b8-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="100b8-119">*lpBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="100b8-119">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="100b8-120">緩衝區的指標，此緩衝區會接收其成員所指向的 [**NDDESHAREINFO**](nddeshareinfo-str.md) 結構和相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="100b8-120">A pointer to a buffer that receives the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure and associated data pointed to by its members.</span></span> <span data-ttu-id="100b8-121">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="100b8-121">This parameter can be **NULL**.</span></span> <span data-ttu-id="100b8-122">如果 *lpBuffer* 為 **Null**，則 DSDM 會計算儲存所要求之共用資訊所需的位元組數目，並在 *lpnTotalAvailable* 欄位中傳回該值，並將該值與 NDDE \_ BUF \_ 太小的錯誤一起傳回 \_ 。</span><span class="sxs-lookup"><span data-stu-id="100b8-122">If *lpBuffer* is **NULL**, then the DSDM calculates the number of bytes required to store the requested share information and returns that value in the *lpnTotalAvailable* field along with the NDDE\_BUF\_TOO\_SMALL error.</span></span>

</dd> <dt>

<span data-ttu-id="100b8-123">*cBufSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="100b8-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100b8-124">*LpBuffer* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="100b8-124">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="100b8-125">如果 *lpBuffer* 為 **Null**，則 *cBufSize* 應為零。</span><span class="sxs-lookup"><span data-stu-id="100b8-125">If *lpBuffer* is **NULL**, then *cBufSize* should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="100b8-126">*lpnTotalAvailable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="100b8-126">*lpnTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="100b8-127">變數的指標，此變數會接收儲存所要求之共用資訊所需的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="100b8-127">A pointer to a variable that receives the total number of bytes needed to store the requested share information.</span></span> <span data-ttu-id="100b8-128">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="100b8-128">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="100b8-129">*lpnItems* \[在\]</span><span class="sxs-lookup"><span data-stu-id="100b8-129">*lpnItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100b8-130">部分共用資訊抓取的專案選取遮罩指標。</span><span class="sxs-lookup"><span data-stu-id="100b8-130">A pointer to an item selection mask for partial share information retrieval.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="100b8-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="100b8-131">Return value</span></span>

<span data-ttu-id="100b8-132">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="100b8-132">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="100b8-133">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="100b8-133">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="100b8-134">如果 *lpBuffer* 參數為 **Null**，則會傳回 NDDE \_ BUF \_ 太 \_ 小。</span><span class="sxs-lookup"><span data-stu-id="100b8-134">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="100b8-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="100b8-135">Requirements</span></span>



| <span data-ttu-id="100b8-136">需求</span><span class="sxs-lookup"><span data-stu-id="100b8-136">Requirement</span></span> | <span data-ttu-id="100b8-137">值</span><span class="sxs-lookup"><span data-stu-id="100b8-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="100b8-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="100b8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="100b8-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="100b8-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="100b8-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="100b8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="100b8-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="100b8-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="100b8-142">標頭</span><span class="sxs-lookup"><span data-stu-id="100b8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="100b8-143"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="100b8-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="100b8-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="100b8-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="100b8-145"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="100b8-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="100b8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="100b8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="100b8-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="100b8-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="100b8-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="100b8-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="100b8-149">**NDdeShareGetInfoW** (Unicode) 和 **NDdeShareGetInfoA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="100b8-149">**NDdeShareGetInfoW** (Unicode) and **NDdeShareGetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="100b8-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="100b8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="100b8-151">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="100b8-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="100b8-152">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="100b8-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="100b8-153">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="100b8-153">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="100b8-154">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="100b8-154">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> </dl>

 

 




