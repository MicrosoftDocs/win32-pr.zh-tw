---
description: 取得列舉順序中的下一個指定資料項目目名稱數目。
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: 'IEnumPStoreItems：： Next 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 967f2f84553b87965d5b2c92d99e347cb259264b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980188"
---
# <a name="ienumpstoreitemsnext-method"></a><span data-ttu-id="18bf6-103">IEnumPStoreItems：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="18bf6-103">IEnumPStoreItems::Next method</span></span>

<span data-ttu-id="18bf6-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="18bf6-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="18bf6-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="18bf6-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="18bf6-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="18bf6-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="18bf6-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="18bf6-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="18bf6-108">取得列舉順序中的下一個指定資料項目目名稱數目。</span><span class="sxs-lookup"><span data-stu-id="18bf6-108">Gets the next specified number of data item names in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="18bf6-109">語法</span><span class="sxs-lookup"><span data-stu-id="18bf6-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="18bf6-110">參數</span><span class="sxs-lookup"><span data-stu-id="18bf6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18bf6-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18bf6-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18bf6-112">要求的資料項目目數。</span><span class="sxs-lookup"><span data-stu-id="18bf6-112">The number of data items requested.</span></span>

</dd> <dt>

<span data-ttu-id="18bf6-113">*rgelt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18bf6-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18bf6-114">要在其中傳回資料項目名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="18bf6-114">A pointer to a string in which to return the data item name.</span></span>

</dd> <dt>

<span data-ttu-id="18bf6-115">*pceltFetched* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="18bf6-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18bf6-116">實際提供的資料項目名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="18bf6-116">A pointer to the number of data item names actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18bf6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="18bf6-117">Return value</span></span>

<span data-ttu-id="18bf6-118">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="18bf6-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="18bf6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="18bf6-119">Requirements</span></span>



| <span data-ttu-id="18bf6-120">需求</span><span class="sxs-lookup"><span data-stu-id="18bf6-120">Requirement</span></span> | <span data-ttu-id="18bf6-121">值</span><span class="sxs-lookup"><span data-stu-id="18bf6-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18bf6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="18bf6-122">Header</span></span><br/> | <dl> <span data-ttu-id="18bf6-123"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="18bf6-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="18bf6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="18bf6-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="18bf6-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18bf6-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18bf6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18bf6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18bf6-127">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="18bf6-127">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
