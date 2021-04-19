---
description: 建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。
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
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001162"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="98fe5-103">IEnumPStoreItems：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="98fe5-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="98fe5-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="98fe5-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="98fe5-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="98fe5-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="98fe5-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="98fe5-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="98fe5-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="98fe5-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="98fe5-108">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="98fe5-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="98fe5-109">語法</span><span class="sxs-lookup"><span data-stu-id="98fe5-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="98fe5-110">參數</span><span class="sxs-lookup"><span data-stu-id="98fe5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98fe5-111">*ppenum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="98fe5-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98fe5-112">指向 [**IEnumPStoreItems**](ienumpstoreitems.md) 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="98fe5-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98fe5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="98fe5-113">Return value</span></span>

<span data-ttu-id="98fe5-114">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="98fe5-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="98fe5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="98fe5-115">Requirements</span></span>



| <span data-ttu-id="98fe5-116">需求</span><span class="sxs-lookup"><span data-stu-id="98fe5-116">Requirement</span></span> | <span data-ttu-id="98fe5-117">值</span><span class="sxs-lookup"><span data-stu-id="98fe5-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98fe5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="98fe5-118">Header</span></span><br/> | <dl> <span data-ttu-id="98fe5-119"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="98fe5-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="98fe5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="98fe5-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="98fe5-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98fe5-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98fe5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98fe5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fe5-123">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="98fe5-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
