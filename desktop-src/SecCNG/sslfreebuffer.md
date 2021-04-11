---
description: 用來釋出安全通訊端層通訊協定 (SSL) 提供者函式所配置的記憶體。
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: 'SslFreeBuffer 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027530"
---
# <a name="sslfreebuffer-function"></a><span data-ttu-id="32f32-103">SslFreeBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="32f32-103">SslFreeBuffer function</span></span>

<span data-ttu-id="32f32-104">**SslFreeBuffer** 函式可用來釋出 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 提供者函式所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="32f32-104">The **SslFreeBuffer** function is used to free memory that was allocated by one of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f32-105">語法</span><span class="sxs-lookup"><span data-stu-id="32f32-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a><span data-ttu-id="32f32-106">參數</span><span class="sxs-lookup"><span data-stu-id="32f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f32-107">*pvInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32f32-107">*pvInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32f32-108">要釋放之記憶體緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="32f32-108">A pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f32-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="32f32-109">Return value</span></span>

<span data-ttu-id="32f32-110">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="32f32-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="32f32-111">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="32f32-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="32f32-112">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="32f32-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="32f32-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="32f32-113">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="32f32-114">Description</span><span class="sxs-lookup"><span data-stu-id="32f32-114">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32f32-115">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="32f32-115"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="32f32-116">*PdwProviderCount* 或 *PpProviderList* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="32f32-116">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32f32-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="32f32-117">Requirements</span></span>



| <span data-ttu-id="32f32-118">需求</span><span class="sxs-lookup"><span data-stu-id="32f32-118">Requirement</span></span> | <span data-ttu-id="32f32-119">值</span><span class="sxs-lookup"><span data-stu-id="32f32-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f32-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32f32-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32f32-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f32-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="32f32-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32f32-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32f32-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f32-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="32f32-124">標頭</span><span class="sxs-lookup"><span data-stu-id="32f32-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f32-125"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="32f32-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="32f32-126">DLL</span><span class="sxs-lookup"><span data-stu-id="32f32-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f32-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f32-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

