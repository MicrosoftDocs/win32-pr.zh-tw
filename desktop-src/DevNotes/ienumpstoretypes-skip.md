---
description: IEnumPStoreTypes：： Skip 方法-略過列舉順序中的下一個指定專案數目。
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'IEnumPStoreTypes：： Skip 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdc656af2a8f50d02d2f88545d189d9c9285a7f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096736"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="088d2-103">IEnumPStoreTypes：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="088d2-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="088d2-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="088d2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="088d2-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="088d2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="088d2-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="088d2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="088d2-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="088d2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="088d2-108">略過列舉順序中的下一個指定專案數目。</span><span class="sxs-lookup"><span data-stu-id="088d2-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="088d2-109">語法</span><span class="sxs-lookup"><span data-stu-id="088d2-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="088d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="088d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="088d2-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="088d2-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="088d2-112">要略過的提供者類型數目。</span><span class="sxs-lookup"><span data-stu-id="088d2-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="088d2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="088d2-113">Return value</span></span>

<span data-ttu-id="088d2-114">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="088d2-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="088d2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="088d2-115">Requirements</span></span>



| <span data-ttu-id="088d2-116">需求</span><span class="sxs-lookup"><span data-stu-id="088d2-116">Requirement</span></span> | <span data-ttu-id="088d2-117">值</span><span class="sxs-lookup"><span data-stu-id="088d2-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="088d2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="088d2-118">Header</span></span><br/> | <dl> <span data-ttu-id="088d2-119"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="088d2-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="088d2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="088d2-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="088d2-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088d2-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="088d2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="088d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088d2-123">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="088d2-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
