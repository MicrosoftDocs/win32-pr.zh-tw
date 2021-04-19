---
description: 起始資料流程的雜湊。
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: 'A_SHAInit 函數 (Sha-1) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986801"
---
# <a name="a_shainit-function"></a><span data-ttu-id="b2172-103">SHAInit 函式 \_</span><span class="sxs-lookup"><span data-stu-id="b2172-103">A\_SHAInit function</span></span>

<span data-ttu-id="b2172-104">起始資料流程的雜湊。</span><span class="sxs-lookup"><span data-stu-id="b2172-104">Initiates the hashing of a stream of data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2172-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2172-105">Syntax</span></span>


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a><span data-ttu-id="b2172-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2172-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2172-107">*內容* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b2172-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2172-108">SHA 內容。</span><span class="sxs-lookup"><span data-stu-id="b2172-108">The SHA context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2172-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2172-109">Return value</span></span>

<span data-ttu-id="b2172-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b2172-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2172-111">備註</span><span class="sxs-lookup"><span data-stu-id="b2172-111">Remarks</span></span>

<span data-ttu-id="b2172-112">此函式與 SHAInit 非常類似，但會直接從程式庫呼叫，而不是透過密碼編譯基礎結構來路由傳送。</span><span class="sxs-lookup"><span data-stu-id="b2172-112">This function is very similar to SHAInit, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="b2172-113">如需詳細資訊，請參閱 [Windows NTCryptographic 提供者](/previous-versions/tn-archive/cc723484(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="b2172-113">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2172-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2172-114">Requirements</span></span>



| <span data-ttu-id="b2172-115">需求</span><span class="sxs-lookup"><span data-stu-id="b2172-115">Requirement</span></span> | <span data-ttu-id="b2172-116">值</span><span class="sxs-lookup"><span data-stu-id="b2172-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2172-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b2172-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b2172-118"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2172-118"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="b2172-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2172-119">Library</span></span><br/> | <dl> <span data-ttu-id="b2172-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2172-120"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2172-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b2172-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b2172-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2172-122"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
