---
description: 不支援 RKeyCloseKeyService 函數。
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: 'RKeyCloseKeyService 函式 (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848043"
---
# <a name="rkeyclosekeyservice-function"></a><span data-ttu-id="bfe88-103">RKeyCloseKeyService 函式</span><span class="sxs-lookup"><span data-stu-id="bfe88-103">RKeyCloseKeyService function</span></span>

<span data-ttu-id="bfe88-104">不支援 **RKeyCloseKeyService** 函數。</span><span class="sxs-lookup"><span data-stu-id="bfe88-104">The **RKeyCloseKeyService** function is not supported.</span></span>

<span data-ttu-id="bfe88-105">**Windows Server 2003：\*\*\*\*RKeyCloseKeyService** 函式會關閉先前呼叫 [**RKeyOpenKeyService**](rkeyopenkeyservice.md)函式所開啟的金鑰服務控制碼。</span><span class="sxs-lookup"><span data-stu-id="bfe88-105">**Windows Server 2003:** The **RKeyCloseKeyService** function closes a key service handle opened by a previous call to the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) function.</span></span> <span data-ttu-id="bfe88-106">請注意，此行為已隨著 Windows Server 2003 Service Pack 1 (SP1) 而變更。</span><span class="sxs-lookup"><span data-stu-id="bfe88-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe88-107">語法</span><span class="sxs-lookup"><span data-stu-id="bfe88-107">Syntax</span></span>


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="bfe88-108">參數</span><span class="sxs-lookup"><span data-stu-id="bfe88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe88-109">*hKeySvcCli* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfe88-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfe88-110">[**RKeyOpenKeyService**](rkeyopenkeyservice.md)先前開啟的 [**KEYSVCC \_ 句**](keysvcc-handle.md)柄控制碼。</span><span class="sxs-lookup"><span data-stu-id="bfe88-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="bfe88-111">此值不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bfe88-111">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bfe88-112">*保留* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bfe88-112">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfe88-113">保留的。</span><span class="sxs-lookup"><span data-stu-id="bfe88-113">Reserved.</span></span> <span data-ttu-id="bfe88-114">將此值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bfe88-114">Set this value to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe88-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfe88-115">Return value</span></span>

<span data-ttu-id="bfe88-116">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="bfe88-116">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="bfe88-117">如果函式失敗，則傳回值為 **ULONG** ，表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="bfe88-117">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe88-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfe88-118">Requirements</span></span>



| <span data-ttu-id="bfe88-119">需求</span><span class="sxs-lookup"><span data-stu-id="bfe88-119">Requirement</span></span> | <span data-ttu-id="bfe88-120">值</span><span class="sxs-lookup"><span data-stu-id="bfe88-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe88-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfe88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe88-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="bfe88-122">None supported</span></span><br/>                                                             |
| <span data-ttu-id="bfe88-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfe88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe88-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfe88-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfe88-125">標頭</span><span class="sxs-lookup"><span data-stu-id="bfe88-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe88-126"><dt>Rkeysvcc。h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe88-126"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfe88-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfe88-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe88-128">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="bfe88-128">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> <dt>

[<span data-ttu-id="bfe88-129">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="bfe88-129">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




