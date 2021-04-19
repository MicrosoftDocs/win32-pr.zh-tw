---
description: 略過列舉順序中的下一個指定專案數目。
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: 'IEnumPStoreProviders：： Skip 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 75ec981e76d387f6ada82869bba40fa4946ce7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976008"
---
# <a name="ienumpstoreprovidersskip-method"></a><span data-ttu-id="77b32-103">IEnumPStoreProviders：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="77b32-103">IEnumPStoreProviders::Skip method</span></span>

<span data-ttu-id="77b32-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="77b32-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="77b32-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="77b32-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="77b32-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="77b32-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="77b32-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="77b32-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="77b32-108">略過列舉順序中的下一個指定專案數目。</span><span class="sxs-lookup"><span data-stu-id="77b32-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b32-109">語法</span><span class="sxs-lookup"><span data-stu-id="77b32-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="77b32-110">參數</span><span class="sxs-lookup"><span data-stu-id="77b32-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b32-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77b32-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b32-112">要略過的提供者類型數目。</span><span class="sxs-lookup"><span data-stu-id="77b32-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77b32-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="77b32-113">Return value</span></span>

<span data-ttu-id="77b32-114">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="77b32-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="77b32-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="77b32-115">Requirements</span></span>



| <span data-ttu-id="77b32-116">需求</span><span class="sxs-lookup"><span data-stu-id="77b32-116">Requirement</span></span> | <span data-ttu-id="77b32-117">值</span><span class="sxs-lookup"><span data-stu-id="77b32-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77b32-118">標頭</span><span class="sxs-lookup"><span data-stu-id="77b32-118">Header</span></span><br/> | <dl> <span data-ttu-id="77b32-119"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="77b32-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="77b32-120">DLL</span><span class="sxs-lookup"><span data-stu-id="77b32-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="77b32-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77b32-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77b32-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77b32-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b32-123">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="77b32-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
