---
description: 不支援 RKeyOpenKeyService 函數。
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: 'RKeyOpenKeyService 函式 (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980387"
---
# <a name="rkeyopenkeyservice-function"></a><span data-ttu-id="104d7-103">RKeyOpenKeyService 函式</span><span class="sxs-lookup"><span data-stu-id="104d7-103">RKeyOpenKeyService function</span></span>

<span data-ttu-id="104d7-104">不支援 **RKeyOpenKeyService** 函數。</span><span class="sxs-lookup"><span data-stu-id="104d7-104">The **RKeyOpenKeyService** function is not supported.</span></span>

<span data-ttu-id="104d7-105">**Windows Server 2003：\*\*\*\*RKeyOpenKeyService** 函式會建立與遠端電腦的連線，並開啟金鑰服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="104d7-105">**Windows Server 2003:** The **RKeyOpenKeyService** function establishes a connection to a remote computer and opens a key service handle.</span></span> <span data-ttu-id="104d7-106">然後， [**RKeyPFXInstall**](rkeypfxinstall.md) 函式可以使用金鑰服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="104d7-106">The key service handle can subsequently be used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span> <span data-ttu-id="104d7-107">請注意，此行為已隨著 Windows Server 2003 Service Pack 1 (SP1) 而變更。</span><span class="sxs-lookup"><span data-stu-id="104d7-107">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="104d7-108">語法</span><span class="sxs-lookup"><span data-stu-id="104d7-108">Syntax</span></span>


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a><span data-ttu-id="104d7-109">參數</span><span class="sxs-lookup"><span data-stu-id="104d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104d7-110">*pszMachineName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="104d7-110">*pszMachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d7-111">表示將開啟金鑰服務控制碼的電腦之以 null 結束之字串的長指標。</span><span class="sxs-lookup"><span data-stu-id="104d7-111">Long pointer to a null-terminated string that represents the computer where the key service handle will be opened.</span></span>

</dd> <dt>

<span data-ttu-id="104d7-112">擁有 *擁有者* \[在\]</span><span class="sxs-lookup"><span data-stu-id="104d7-112">*OwnerType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d7-113">[**KEYSVC \_**](keysvc-type.md)代表索引鍵類型的類型值。</span><span class="sxs-lookup"><span data-stu-id="104d7-113">[**KEYSVC\_TYPE**](keysvc-type.md) value that represents the key type.</span></span> <span data-ttu-id="104d7-114">唯一支援的值為 **KeySvcMachine**。</span><span class="sxs-lookup"><span data-stu-id="104d7-114">The only supported value is **KeySvcMachine**.</span></span>

</dd> <dt>

<span data-ttu-id="104d7-115">*pwszOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="104d7-115">*pwszOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d7-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="104d7-116">Reserved.</span></span> <span data-ttu-id="104d7-117">將此值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="104d7-117">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="104d7-118">*pAuthentication* \[在\]</span><span class="sxs-lookup"><span data-stu-id="104d7-118">*pAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d7-119">**Void** 的指標，表示驗證設定。</span><span class="sxs-lookup"><span data-stu-id="104d7-119">A pointer to a **void** that represents the authentication settings.</span></span> <span data-ttu-id="104d7-120">此指標可以指向值為零或以下的值。</span><span class="sxs-lookup"><span data-stu-id="104d7-120">This pointer can point to a value of zero or the following value.</span></span>



| <span data-ttu-id="104d7-121">值</span><span class="sxs-lookup"><span data-stu-id="104d7-121">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="104d7-122">意義</span><span class="sxs-lookup"><span data-stu-id="104d7-122">Meaning</span></span>                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <span data-ttu-id="104d7-123"><dt>**RKEYSVC \_\_ \_ 僅連接安全**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="104d7-123"><dt>**RKEYSVC\_CONNECT\_SECURE\_ONLY**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="104d7-124">用戶端需要相互驗證。</span><span class="sxs-lookup"><span data-stu-id="104d7-124">The client requires mutual authentication.</span></span> <span data-ttu-id="104d7-125">如果指定此值，則回復到 NTLM 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="104d7-125">If this value is specified, fallback to NTLM will fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="104d7-126">*保留* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="104d7-126">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="104d7-127">保留的。</span><span class="sxs-lookup"><span data-stu-id="104d7-127">Reserved.</span></span> <span data-ttu-id="104d7-128">將此值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="104d7-128">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="104d7-129">*phKeySvcCli* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="104d7-129">*phKeySvcCli* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="104d7-130">[**KEYSVCC \_ 控制碼**](keysvcc-handle.md)的指標，該控制碼會接收開啟的金鑰服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="104d7-130">A pointer to a [**KEYSVCC\_HANDLE**](keysvcc-handle.md) that receives the opened key service handle.</span></span> <span data-ttu-id="104d7-131">當您完成使用控制碼時，請呼叫 [**RKeyCloseKeyService**](rkeyclosekeyservice.md) 函式來釋放資源。</span><span class="sxs-lookup"><span data-stu-id="104d7-131">When you have finished using the handle, free the resource by calling the [**RKeyCloseKeyService**](rkeyclosekeyservice.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104d7-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="104d7-132">Return value</span></span>

<span data-ttu-id="104d7-133">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="104d7-133">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="104d7-134">如果函式失敗，則傳回值為 **ULONG** ，表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="104d7-134">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="104d7-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="104d7-135">Requirements</span></span>



| <span data-ttu-id="104d7-136">需求</span><span class="sxs-lookup"><span data-stu-id="104d7-136">Requirement</span></span> | <span data-ttu-id="104d7-137">值</span><span class="sxs-lookup"><span data-stu-id="104d7-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="104d7-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="104d7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="104d7-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="104d7-139">None supported</span></span><br/>                                                             |
| <span data-ttu-id="104d7-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="104d7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="104d7-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="104d7-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="104d7-142">標頭</span><span class="sxs-lookup"><span data-stu-id="104d7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="104d7-143"><dt>Rkeysvcc。h</dt></span><span class="sxs-lookup"><span data-stu-id="104d7-143"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="104d7-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="104d7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104d7-145">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="104d7-145">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="104d7-146">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="104d7-146">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




