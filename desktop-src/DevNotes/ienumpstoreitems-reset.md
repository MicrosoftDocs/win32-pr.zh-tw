---
description: 重設為指定列舉序列的開頭。
ms.assetid: add91f5d-3f84-4069-93c0-9380a3935b85
title: 'IEnumPStoreItems：： Reset 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d5b05c23ba40ab647b2c4b3bb552f92ee34e12c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999480"
---
# <a name="ienumpstoreitemsreset-method"></a><span data-ttu-id="67aa9-103">IEnumPStoreItems：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="67aa9-103">IEnumPStoreItems::Reset method</span></span>

<span data-ttu-id="67aa9-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="67aa9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="67aa9-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="67aa9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="67aa9-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="67aa9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="67aa9-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="67aa9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="67aa9-108">重設為指定列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="67aa9-108">Resets to the beginning of the given enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="67aa9-109">語法</span><span class="sxs-lookup"><span data-stu-id="67aa9-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="67aa9-110">參數</span><span class="sxs-lookup"><span data-stu-id="67aa9-110">Parameters</span></span>

<span data-ttu-id="67aa9-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="67aa9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67aa9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="67aa9-112">Return value</span></span>

<span data-ttu-id="67aa9-113">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="67aa9-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="67aa9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="67aa9-114">Requirements</span></span>



| <span data-ttu-id="67aa9-115">需求</span><span class="sxs-lookup"><span data-stu-id="67aa9-115">Requirement</span></span> | <span data-ttu-id="67aa9-116">值</span><span class="sxs-lookup"><span data-stu-id="67aa9-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67aa9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="67aa9-117">Header</span></span><br/> | <dl> <span data-ttu-id="67aa9-118"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="67aa9-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="67aa9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="67aa9-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="67aa9-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67aa9-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67aa9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67aa9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67aa9-122">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="67aa9-122">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
