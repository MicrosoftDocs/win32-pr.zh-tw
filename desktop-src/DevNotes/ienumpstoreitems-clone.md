---
description: IEnumPStoreItems：： Clone 方法-建立另一個列舉值，其中包含與目前相同的列舉狀態。
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'IEnumPStoreItems：： Clone 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 29b618881305296a560dc9102f7571c08236d1bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089326"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="fb0d1-103">IEnumPStoreItems：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="fb0d1-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="fb0d1-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="fb0d1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="fb0d1-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="fb0d1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="fb0d1-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="fb0d1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="fb0d1-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="fb0d1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="fb0d1-108">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="fb0d1-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb0d1-109">語法</span><span class="sxs-lookup"><span data-stu-id="fb0d1-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="fb0d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb0d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb0d1-111">*ppenum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb0d1-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0d1-112">指向 [**IEnumPStoreItems**](ienumpstoreitems.md) 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="fb0d1-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb0d1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb0d1-113">Return value</span></span>

<span data-ttu-id="fb0d1-114">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="fb0d1-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb0d1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb0d1-115">Requirements</span></span>



| <span data-ttu-id="fb0d1-116">需求</span><span class="sxs-lookup"><span data-stu-id="fb0d1-116">Requirement</span></span> | <span data-ttu-id="fb0d1-117">值</span><span class="sxs-lookup"><span data-stu-id="fb0d1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb0d1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="fb0d1-118">Header</span></span><br/> | <dl> <span data-ttu-id="fb0d1-119"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb0d1-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="fb0d1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fb0d1-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="fb0d1-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb0d1-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb0d1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb0d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb0d1-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="fb0d1-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
