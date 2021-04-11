---
description: 根據 RFC 5705 標準匯出金鑰內容。
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: 'SslExportKeyingMaterial 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695379"
---
# <a name="sslexportkeyingmaterial-function"></a><span data-ttu-id="18548-103">SslExportKeyingMaterial 函式</span><span class="sxs-lookup"><span data-stu-id="18548-103">SslExportKeyingMaterial function</span></span>

<span data-ttu-id="18548-104">根據 [RFC 5705 標準](https://tools.ietf.org/html/rfc5705)匯出金鑰內容。</span><span class="sxs-lookup"><span data-stu-id="18548-104">Exports keying material per the [RFC 5705 standard](https://tools.ietf.org/html/rfc5705).</span></span> <span data-ttu-id="18548-105">此函式會使用 TLS 的非虛擬亂數函式來產生金鑰內容的位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18548-105">This function uses the TLS pseudorandom function to produce a byte buffer of keying material.</span></span> <span data-ttu-id="18548-106">它會參考主要密碼、disambiguating ASCII 標籤、用戶端和伺服器隨機值，以及選擇性的應用程式內容資料。</span><span class="sxs-lookup"><span data-stu-id="18548-106">It takes a reference to the master secret, the disambiguating ASCII label, client and server random values, and optionally the application context data.</span></span>

## <a name="syntax"></a><span data-ttu-id="18548-107">語法</span><span class="sxs-lookup"><span data-stu-id="18548-107">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="18548-108">參數</span><span class="sxs-lookup"><span data-stu-id="18548-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18548-109">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-109">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-110">TLS 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="18548-110">The handle of the TLS protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="18548-111">*hMasterKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-111">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-112">主要金鑰組象的控制碼，該物件將用來建立已匯出至 br 的金鑰處理內容。</span><span class="sxs-lookup"><span data-stu-id="18548-112">The handle of the master key object that will be used to create the keying material to br exported.</span></span>

</dd> <dt>

<span data-ttu-id="18548-113">*sLabel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-113">*sLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-114">以 NUL 終止的 ASCII 標籤字串。</span><span class="sxs-lookup"><span data-stu-id="18548-114">a NUL-terminated ASCII label string.</span></span> <span data-ttu-id="18548-115">Schannel 會先移除終止的 NUL 字元，再將它傳遞給虛擬亂數函式。</span><span class="sxs-lookup"><span data-stu-id="18548-115">Schannel will remove the terminating NUL character before passing it to the pseudorandom function.</span></span>

</dd> <dt>

<span data-ttu-id="18548-116">*pbRandoms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-116">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-117">包含 *用戶端 \_ 隨機* 和 *伺服器 \_ 隨機* 值（TLS 連接）串連的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="18548-117">A pointer to a buffer that contains a concatenation of the *client\_random* and *server\_random* values of the TLS connection.</span></span>

</dd> <dt>

<span data-ttu-id="18548-118">*cbRandoms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-118">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-119">*PbRandoms* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="18548-119">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="18548-120">*pbCoNtextValue* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18548-120">*pbContextValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-121">包含應用程式內容的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="18548-121">A pointer to a buffer that contains the application context.</span></span> <span data-ttu-id="18548-122">如果 *pbCoNtextValue* 為 **Null**，則 *cbCoNtextValue* 必須為零。</span><span class="sxs-lookup"><span data-stu-id="18548-122">If *pbContextValue* is **NULL**, *cbContextValue* must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="18548-123">*cbCoNtextValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-123">*cbContextValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-124">*PbCoNtextValue* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="18548-124">The length, in bytes, of the *pbContextValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="18548-125">*pbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18548-125">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-126">接收匯出的金鑰內容的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="18548-126">The address of a buffer that receives the exported keying material.</span></span> <span data-ttu-id="18548-127">*CbOutput* 參數包含這個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="18548-127">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="18548-128">此值不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18548-128">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="18548-129">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-129">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-130">*PbOutput* 緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="18548-130">The length, in bytes, of the *pbOutput* buffer.</span></span> <span data-ttu-id="18548-131">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="18548-131">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="18548-132">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18548-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18548-133">未使用。</span><span class="sxs-lookup"><span data-stu-id="18548-133">Not used.</span></span> <span data-ttu-id="18548-134">必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="18548-134">Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18548-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="18548-135">Return value</span></span>

<span data-ttu-id="18548-136">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="18548-136">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="18548-137">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="18548-137">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="18548-138">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="18548-138">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="18548-139">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="18548-139">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="18548-140">Description</span><span class="sxs-lookup"><span data-stu-id="18548-140">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="18548-141">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="18548-141"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="18548-142">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="18548-142">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18548-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="18548-143">Requirements</span></span>



| <span data-ttu-id="18548-144">需求</span><span class="sxs-lookup"><span data-stu-id="18548-144">Requirement</span></span> | <span data-ttu-id="18548-145">值</span><span class="sxs-lookup"><span data-stu-id="18548-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18548-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18548-146">Minimum supported client</span></span><br/> | <span data-ttu-id="18548-147">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18548-147">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="18548-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18548-148">Minimum supported server</span></span><br/> | <span data-ttu-id="18548-149">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18548-149">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="18548-150">標頭</span><span class="sxs-lookup"><span data-stu-id="18548-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="18548-151"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="18548-151"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="18548-152">DLL</span><span class="sxs-lookup"><span data-stu-id="18548-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18548-153"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18548-153"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




