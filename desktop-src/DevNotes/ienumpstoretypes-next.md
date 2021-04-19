---
description: 取得列舉順序中的下一個指定的提供者類型數目。
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'IEnumPStoreTypes：： Next 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 18981053de897b75d1febdc75e138e6561e65bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996457"
---
# <a name="ienumpstoretypesnext-method"></a><span data-ttu-id="473fd-103">IEnumPStoreTypes：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="473fd-103">IEnumPStoreTypes::Next method</span></span>

<span data-ttu-id="473fd-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="473fd-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="473fd-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="473fd-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="473fd-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="473fd-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="473fd-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="473fd-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="473fd-108">取得列舉順序中的下一個指定的提供者類型數目。</span><span class="sxs-lookup"><span data-stu-id="473fd-108">Gets the next specified number of provider types in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="473fd-109">語法</span><span class="sxs-lookup"><span data-stu-id="473fd-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="473fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="473fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="473fd-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="473fd-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="473fd-112">要求的提供者類型數目。</span><span class="sxs-lookup"><span data-stu-id="473fd-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="473fd-113">*rgelt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="473fd-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="473fd-114">要在其中傳回提供者類型名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="473fd-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="473fd-115">*pceltFetched* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="473fd-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="473fd-116">實際提供的提供者類型數目的指標。</span><span class="sxs-lookup"><span data-stu-id="473fd-116">A pointer to the number of provider types actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="473fd-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="473fd-117">Return value</span></span>

<span data-ttu-id="473fd-118">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="473fd-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="473fd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="473fd-119">Requirements</span></span>



| <span data-ttu-id="473fd-120">需求</span><span class="sxs-lookup"><span data-stu-id="473fd-120">Requirement</span></span> | <span data-ttu-id="473fd-121">值</span><span class="sxs-lookup"><span data-stu-id="473fd-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="473fd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="473fd-122">Header</span></span><br/> | <dl> <span data-ttu-id="473fd-123"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="473fd-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="473fd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="473fd-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="473fd-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="473fd-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="473fd-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="473fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473fd-127">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="473fd-127">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
