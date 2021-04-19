---
description: 重設為列舉序列的開頭。
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: 'IEnumPStoreTypes：： Reset 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 60aeb1f68bcbf18e903472fa736b5714076dfbfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986180"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="1a194-103">IEnumPStoreTypes：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="1a194-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="1a194-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1a194-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="1a194-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="1a194-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="1a194-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="1a194-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="1a194-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="1a194-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="1a194-108">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="1a194-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a194-109">語法</span><span class="sxs-lookup"><span data-stu-id="1a194-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="1a194-110">參數</span><span class="sxs-lookup"><span data-stu-id="1a194-110">Parameters</span></span>

<span data-ttu-id="1a194-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1a194-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a194-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a194-112">Return value</span></span>

<span data-ttu-id="1a194-113">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1a194-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a194-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a194-114">Requirements</span></span>



| <span data-ttu-id="1a194-115">需求</span><span class="sxs-lookup"><span data-stu-id="1a194-115">Requirement</span></span> | <span data-ttu-id="1a194-116">值</span><span class="sxs-lookup"><span data-stu-id="1a194-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a194-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1a194-117">Header</span></span><br/> | <dl> <span data-ttu-id="1a194-118"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a194-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="1a194-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1a194-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="1a194-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a194-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a194-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a194-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a194-122">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="1a194-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
