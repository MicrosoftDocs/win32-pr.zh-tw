---
description: 建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'IEnumPStoreProviders：： Clone 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdd7825a44dcea672eff24a15126921f0426a986
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995779"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="0ea69-103">IEnumPStoreProviders：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="0ea69-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="0ea69-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="0ea69-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0ea69-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="0ea69-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0ea69-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="0ea69-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0ea69-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="0ea69-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0ea69-108">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="0ea69-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea69-109">語法</span><span class="sxs-lookup"><span data-stu-id="0ea69-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="0ea69-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ea69-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea69-111">*ppenum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0ea69-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea69-112">指向 [**IEnumPStoreProviders**](ienumpstoreproviders.md) 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="0ea69-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea69-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ea69-113">Return value</span></span>

<span data-ttu-id="0ea69-114">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0ea69-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea69-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ea69-115">Requirements</span></span>



| <span data-ttu-id="0ea69-116">需求</span><span class="sxs-lookup"><span data-stu-id="0ea69-116">Requirement</span></span> | <span data-ttu-id="0ea69-117">值</span><span class="sxs-lookup"><span data-stu-id="0ea69-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea69-118">標頭</span><span class="sxs-lookup"><span data-stu-id="0ea69-118">Header</span></span><br/> | <dl> <span data-ttu-id="0ea69-119"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea69-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0ea69-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea69-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="0ea69-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ea69-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea69-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ea69-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea69-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="0ea69-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
