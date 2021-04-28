---
description: IEnumPStoreProviders：： Reset 方法-重設為列舉序列的開頭。
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: 'IEnumPStoreProviders：： Reset 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3e37e131b6f67f94bb787051123be8eb430eb39e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096756"
---
# <a name="ienumpstoreprovidersreset-method"></a><span data-ttu-id="17957-103">IEnumPStoreProviders：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="17957-103">IEnumPStoreProviders::Reset method</span></span>

<span data-ttu-id="17957-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="17957-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="17957-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="17957-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="17957-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="17957-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="17957-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="17957-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="17957-108">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="17957-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="17957-109">語法</span><span class="sxs-lookup"><span data-stu-id="17957-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="17957-110">參數</span><span class="sxs-lookup"><span data-stu-id="17957-110">Parameters</span></span>

<span data-ttu-id="17957-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="17957-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17957-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="17957-112">Return value</span></span>

<span data-ttu-id="17957-113">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="17957-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="17957-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="17957-114">Requirements</span></span>



| <span data-ttu-id="17957-115">需求</span><span class="sxs-lookup"><span data-stu-id="17957-115">Requirement</span></span> | <span data-ttu-id="17957-116">值</span><span class="sxs-lookup"><span data-stu-id="17957-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17957-117">標頭</span><span class="sxs-lookup"><span data-stu-id="17957-117">Header</span></span><br/> | <dl> <span data-ttu-id="17957-118"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="17957-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="17957-119">DLL</span><span class="sxs-lookup"><span data-stu-id="17957-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="17957-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17957-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17957-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17957-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17957-122">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="17957-122">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
