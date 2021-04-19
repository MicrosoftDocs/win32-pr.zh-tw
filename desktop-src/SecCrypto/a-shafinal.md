---
description: 計算 MD5Update 函數所輸入之資料的最終雜湊。
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: 'A_SHAFinal 函數 (Sha-1) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994574"
---
# <a name="a_shafinal-function"></a><span data-ttu-id="f82b1-103">SHAFinal 函式 \_</span><span class="sxs-lookup"><span data-stu-id="f82b1-103">A\_SHAFinal function</span></span>

<span data-ttu-id="f82b1-104">計算 MD5Update 函數所輸入之資料的最終雜湊。</span><span class="sxs-lookup"><span data-stu-id="f82b1-104">Computes the final hash of the data entered by the MD5Update function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f82b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="f82b1-105">Syntax</span></span>


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a><span data-ttu-id="f82b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f82b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f82b1-107">*內容* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f82b1-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f82b1-108">SHA 內容。</span><span class="sxs-lookup"><span data-stu-id="f82b1-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="f82b1-109">*結果* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f82b1-109">*Result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f82b1-110">產生的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f82b1-110">The resulting hash table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f82b1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f82b1-111">Return value</span></span>

<span data-ttu-id="f82b1-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f82b1-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f82b1-113">備註</span><span class="sxs-lookup"><span data-stu-id="f82b1-113">Remarks</span></span>

<span data-ttu-id="f82b1-114">此函式與 SHAFinal 非常類似，但會直接從程式庫呼叫，而不是透過密碼編譯基礎結構來路由傳送。</span><span class="sxs-lookup"><span data-stu-id="f82b1-114">This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="f82b1-115">如需詳細資訊，請參閱 [Windows NTCryptographic 提供者](/previous-versions/tn-archive/cc723484(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="f82b1-115">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f82b1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f82b1-116">Requirements</span></span>



| <span data-ttu-id="f82b1-117">需求</span><span class="sxs-lookup"><span data-stu-id="f82b1-117">Requirement</span></span> | <span data-ttu-id="f82b1-118">值</span><span class="sxs-lookup"><span data-stu-id="f82b1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f82b1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f82b1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f82b1-120"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="f82b1-120"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="f82b1-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="f82b1-121">Library</span></span><br/> | <dl> <span data-ttu-id="f82b1-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f82b1-122"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="f82b1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f82b1-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f82b1-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f82b1-124"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
