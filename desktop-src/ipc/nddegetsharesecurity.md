---
description: 抓取與 DDE 共用相關聯的安全描述項。 這通常是用來進行編輯。
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: 'NDdeGetShareSecurity 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852236"
---
# <a name="nddegetsharesecurity-function"></a><span data-ttu-id="b4606-104">NDdeGetShareSecurity 函式</span><span class="sxs-lookup"><span data-stu-id="b4606-104">NDdeGetShareSecurity function</span></span>

<span data-ttu-id="b4606-105">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="b4606-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b4606-106">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="b4606-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b4606-107">抓取與 DDE 共用相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b4606-107">Retrieves the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="b4606-108">這通常是用來進行編輯。</span><span class="sxs-lookup"><span data-stu-id="b4606-108">This is done usually for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4606-109">語法</span><span class="sxs-lookup"><span data-stu-id="b4606-109">Syntax</span></span>


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a><span data-ttu-id="b4606-110">參數</span><span class="sxs-lookup"><span data-stu-id="b4606-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4606-111">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4606-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4606-112">DSDM 所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b4606-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="b4606-113">*lpszShareName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4606-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4606-114">要從 DSDM 中取出其安全描述項的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="b4606-114">The name of the share whose security descriptor is to be retrieved from the DSDM.</span></span> <span data-ttu-id="b4606-115">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4606-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4606-116">*si* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4606-116">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4606-117">[**安全性 \_ 資訊**](/windows/desktop/SecAuthZ/security-information)值，指定要從與共享相關聯的安全描述項中取出的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="b4606-117">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that specifies the security information to be retrieved from the security descriptor associated with the share.</span></span>

</dd> <dt>

<span data-ttu-id="b4606-118">*pSD* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b4606-118">*pSD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4606-119">[**安全性 \_ 描述**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)元結構的指標，該結構會接收自我相關的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b4606-119">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that receives the self-relative security descriptor.</span></span> <span data-ttu-id="b4606-120">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4606-120">This parameter can be **NULL**.</span></span> <span data-ttu-id="b4606-121">如果此參數為 **Null**，則 DSDM 會判斷要求的安全性資訊大小，並傳回 *lpcbsdRequired* 參數中所需的位元組數目，以及 NDDE \_ BUF \_ 太小的 \_ 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b4606-121">If this parameter is **NULL**, the DSDM determines the size of the requested security information and returns the number of bytes needed in the *lpcbsdRequired* parameter along with the NDDE\_BUF\_TOO\_SMALL error code.</span></span>

</dd> <dt>

<span data-ttu-id="b4606-122">*cbSD* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4606-122">*cbSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4606-123">*PSD* 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="b4606-123">The size of the *pSD* buffer.</span></span> <span data-ttu-id="b4606-124">如果 *pSD* 為 **Null**，則此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="b4606-124">This parameter must be zero if *pSD* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4606-125">*lpcbsdRequired* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b4606-125">*lpcbsdRequired* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4606-126">變數的指標，此變數會接收所抓取之安全描述項的實際大小。</span><span class="sxs-lookup"><span data-stu-id="b4606-126">A pointer to the variable that receives the actual size of the retrieved security descriptor.</span></span> <span data-ttu-id="b4606-127">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4606-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4606-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4606-128">Return value</span></span>

<span data-ttu-id="b4606-129">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="b4606-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="b4606-130">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b4606-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="b4606-131">如果 *pSD* 參數為 **Null**，則會傳回 NDDE \_ BUF \_ 太 \_ 小。</span><span class="sxs-lookup"><span data-stu-id="b4606-131">If the *pSD* parameter was **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4606-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4606-132">Requirements</span></span>



| <span data-ttu-id="b4606-133">需求</span><span class="sxs-lookup"><span data-stu-id="b4606-133">Requirement</span></span> | <span data-ttu-id="b4606-134">值</span><span class="sxs-lookup"><span data-stu-id="b4606-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4606-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4606-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b4606-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4606-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b4606-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4606-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b4606-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4606-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b4606-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b4606-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4606-140"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4606-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4606-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="b4606-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4606-142"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4606-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4606-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b4606-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4606-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4606-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4606-145">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b4606-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b4606-146">**NDdeGetShareSecurityW** (Unicode) 和 **NDdeGetShareSecurityA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b4606-146">**NDdeGetShareSecurityW** (Unicode) and **NDdeGetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="b4606-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4606-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4606-148">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="b4606-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b4606-149">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="b4606-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="b4606-150">**安全性 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b4606-150">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="b4606-151">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="b4606-151">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> </dl>

 

