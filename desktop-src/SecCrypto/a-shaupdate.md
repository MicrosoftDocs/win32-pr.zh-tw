---
description: 將資料加入至指定的雜湊物件。
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: 'A_SHAUpdate 函數 (Sha-1) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995913"
---
# <a name="a_shaupdate-function"></a><span data-ttu-id="41d20-103">SHAUpdate 函式 \_</span><span class="sxs-lookup"><span data-stu-id="41d20-103">A\_SHAUpdate function</span></span>

<span data-ttu-id="41d20-104">將資料加入至指定的雜湊物件。</span><span class="sxs-lookup"><span data-stu-id="41d20-104">Adds data to a specified hash object.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d20-105">語法</span><span class="sxs-lookup"><span data-stu-id="41d20-105">Syntax</span></span>


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="41d20-106">參數</span><span class="sxs-lookup"><span data-stu-id="41d20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d20-107">*內容* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="41d20-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d20-108">SHA 內容。</span><span class="sxs-lookup"><span data-stu-id="41d20-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="41d20-109">*緩衝區* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="41d20-109">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d20-110">雜湊表。</span><span class="sxs-lookup"><span data-stu-id="41d20-110">The hash table.</span></span>

</dd> <dt>

<span data-ttu-id="41d20-111">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="41d20-111">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="41d20-112">緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="41d20-112">The size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d20-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="41d20-113">Return value</span></span>

<span data-ttu-id="41d20-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="41d20-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d20-115">備註</span><span class="sxs-lookup"><span data-stu-id="41d20-115">Remarks</span></span>

<span data-ttu-id="41d20-116">您可以多次呼叫此函數，以計算長資料流程或不連續資料流程的雜湊。</span><span class="sxs-lookup"><span data-stu-id="41d20-116">This function can be called multiple times to compute the hash on long data streams or discontinuous data streams.</span></span> <span data-ttu-id="41d20-117">在抓取雜湊值之前，必須先呼叫 [**\_ SHAFinal**](a-shafinal.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="41d20-117">The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.</span></span>

<span data-ttu-id="41d20-118">此函式與 SHAUpdate 非常類似，但會直接從程式庫呼叫，而不是透過密碼編譯基礎結構來路由傳送。</span><span class="sxs-lookup"><span data-stu-id="41d20-118">This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="41d20-119">如需詳細資訊，請參閱 [Windows NTCryptographic 提供者](/previous-versions/tn-archive/cc723484(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="41d20-119">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="41d20-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="41d20-120">Requirements</span></span>



| <span data-ttu-id="41d20-121">需求</span><span class="sxs-lookup"><span data-stu-id="41d20-121">Requirement</span></span> | <span data-ttu-id="41d20-122">值</span><span class="sxs-lookup"><span data-stu-id="41d20-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41d20-123">標頭</span><span class="sxs-lookup"><span data-stu-id="41d20-123">Header</span></span><br/>  | <dl> <span data-ttu-id="41d20-124"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d20-124"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="41d20-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="41d20-125">Library</span></span><br/> | <dl> <span data-ttu-id="41d20-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d20-126"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="41d20-127">DLL</span><span class="sxs-lookup"><span data-stu-id="41d20-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="41d20-128"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d20-128"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
