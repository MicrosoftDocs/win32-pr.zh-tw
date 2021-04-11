---
description: 開啟指定安全通訊端層通訊協定 (SSL) 通訊協定提供者的控制碼。
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: 'SslOpenProvider 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191261"
---
# <a name="sslopenprovider-function"></a><span data-ttu-id="1fa59-103">SslOpenProvider 函式</span><span class="sxs-lookup"><span data-stu-id="1fa59-103">SslOpenProvider function</span></span>

<span data-ttu-id="1fa59-104">**SslOpenProvider** 函式會開啟指定 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1fa59-104">The **SslOpenProvider** function opens a handle to the specified [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa59-105">語法</span><span class="sxs-lookup"><span data-stu-id="1fa59-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1fa59-106">參數</span><span class="sxs-lookup"><span data-stu-id="1fa59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa59-107">*phSslProvider* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1fa59-107">*phSslProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa59-108">要在其中寫入提供者控制碼的 **NCRYPT \_ >prov \_ 控制碼** 位址。</span><span class="sxs-lookup"><span data-stu-id="1fa59-108">The address of an **NCRYPT\_PROV\_HANDLE** in which to write the provider handle.</span></span>

<span data-ttu-id="1fa59-109">當您完成使用控制碼時，您應該呼叫 [**SslFreeObject**](sslfreeobject.md) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="1fa59-109">When you have finished using the handle, you should free it by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1fa59-110">*pszProviderName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fa59-110">*pszProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa59-111">Unicode 字串的指標，其中包含提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa59-111">A pointer to a Unicode string that contains the provider name.</span></span> <span data-ttu-id="1fa59-112">如果這個參數的值為 **Null**，則會傳回 **MS \_ SCHANNEL \_ 提供者** 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1fa59-112">If the value of this parameter is **NULL**, a handle to the **MS\_SCHANNEL\_PROVIDER** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="1fa59-113">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fa59-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa59-114">此參數會保留供日後使用，且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="1fa59-114">This parameter is reserved for future use, and it must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fa59-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fa59-115">Return value</span></span>

<span data-ttu-id="1fa59-116">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1fa59-116">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="1fa59-117">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="1fa59-117">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="1fa59-118">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="1fa59-118">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="1fa59-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1fa59-119">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="1fa59-120">Description</span><span class="sxs-lookup"><span data-stu-id="1fa59-120">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fa59-121">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="1fa59-121"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="1fa59-122">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="1fa59-122">One of the provided handles is not valid.</span></span><br/>                      |
| <dl> <span data-ttu-id="1fa59-123">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="1fa59-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="1fa59-124">*PhSslProvider* 或 *PpProviderList* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1fa59-124">The *phSslProvider* or *ppProviderList* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="1fa59-125"><dt>**狀態 \_沒有 \_ 記憶體**</dt> <dt>0xC0000017L</dt></span><span class="sxs-lookup"><span data-stu-id="1fa59-125"><dt>**STATUS\_NO\_MEMORY**</dt> <dt>0xC0000017L</dt></span></span> </dl>      | <span data-ttu-id="1fa59-126">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1fa59-126">Not enough memory is available to allocate necessary buffers.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="1fa59-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fa59-127">Requirements</span></span>



| <span data-ttu-id="1fa59-128">需求</span><span class="sxs-lookup"><span data-stu-id="1fa59-128">Requirement</span></span> | <span data-ttu-id="1fa59-129">值</span><span class="sxs-lookup"><span data-stu-id="1fa59-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa59-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fa59-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa59-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fa59-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1fa59-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fa59-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa59-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fa59-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1fa59-134">標頭</span><span class="sxs-lookup"><span data-stu-id="1fa59-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fa59-135"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa59-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="1fa59-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa59-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa59-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa59-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

