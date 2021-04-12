---
description: 抓取呼叫進程內容中受信任之所有網路 DDE 共用的名稱。
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: 'NDdeTrustedShareEnum 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320275"
---
# <a name="nddetrustedshareenum-function"></a><span data-ttu-id="c0b90-103">NDdeTrustedShareEnum 函式</span><span class="sxs-lookup"><span data-stu-id="c0b90-103">NDdeTrustedShareEnum function</span></span>

<span data-ttu-id="c0b90-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="c0b90-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="c0b90-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="c0b90-106">抓取呼叫進程內容中受信任之所有網路 DDE 共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b90-106">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b90-107">語法</span><span class="sxs-lookup"><span data-stu-id="c0b90-107">Syntax</span></span>


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="c0b90-108">參數</span><span class="sxs-lookup"><span data-stu-id="c0b90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b90-109">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b90-110">DSDM 所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b90-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="c0b90-111">*nLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b90-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="c0b90-112">Reserved.</span></span> <span data-ttu-id="c0b90-113">此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="c0b90-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0b90-114">*lpBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b90-115">接收受信任的 DDE 共用清單的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="c0b90-115">A pointer to a buffer that receives the list of trusted DDE shares.</span></span> <span data-ttu-id="c0b90-116">受信任的 DDE 共用清單會以一系列以 null 分隔的字串，以結尾是雙 null 字元結束的順序傳回。</span><span class="sxs-lookup"><span data-stu-id="c0b90-116">The list of trusted DDE shares is returned as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="c0b90-117">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c0b90-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="c0b90-118">如果 *lpBuffer* 為 **Null**，則 DSDM 會傳回在 *lpcbTotalAvailable* 欄位中保存共用清單所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="c0b90-118">If the *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* field.</span></span>

</dd> <dt>

<span data-ttu-id="c0b90-119">*cBufSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b90-120">*LpBuffer* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c0b90-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="c0b90-121">如果 *lpBuffer* 為 **Null**，則此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="c0b90-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c0b90-122">*lpnEntriesRead* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b90-123">變數的指標，此變數會接收所列舉之受信任共用的總計數。</span><span class="sxs-lookup"><span data-stu-id="c0b90-123">A pointer to a variable that receives the total number of trusted shares being enumerated.</span></span> <span data-ttu-id="c0b90-124">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c0b90-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c0b90-125">*lpcbTotalAvailable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b90-126">變數的指標，此變數會接收儲存受信任的 DDE 共用清單所需的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="c0b90-126">A pointer to a variable that receives the total number of bytes needed to store the list of trusted DDE shares.</span></span> <span data-ttu-id="c0b90-127">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c0b90-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b90-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0b90-128">Return value</span></span>

<span data-ttu-id="c0b90-129">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="c0b90-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="c0b90-130">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="c0b90-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="c0b90-131">如果 *lpBuffer* 參數為 **Null**，則會傳回 NDDE \_ BUF \_ 太 \_ 小。</span><span class="sxs-lookup"><span data-stu-id="c0b90-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b90-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0b90-132">Requirements</span></span>



| <span data-ttu-id="c0b90-133">需求</span><span class="sxs-lookup"><span data-stu-id="c0b90-133">Requirement</span></span> | <span data-ttu-id="c0b90-134">值</span><span class="sxs-lookup"><span data-stu-id="c0b90-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b90-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0b90-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b90-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c0b90-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0b90-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b90-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0b90-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c0b90-139">標頭</span><span class="sxs-lookup"><span data-stu-id="c0b90-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b90-140"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b90-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0b90-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="c0b90-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0b90-142"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0b90-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0b90-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c0b90-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b90-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b90-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0b90-145">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c0b90-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c0b90-146">**NDdeTrustedShareEnumW** (Unicode) 和 **NDdeTrustedShareEnumA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c0b90-146">**NDdeTrustedShareEnumW** (Unicode) and **NDdeTrustedShareEnumA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="c0b90-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0b90-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b90-148">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="c0b90-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="c0b90-149">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="c0b90-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




