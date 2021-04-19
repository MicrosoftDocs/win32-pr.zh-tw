---
description: 用於設定指定的參數資訊。
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'IPStore：： GetProvParam 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977598"
---
# <a name="ipstoregetprovparam-method"></a><span data-ttu-id="700d5-103">IPStore：： GetProvParam 方法</span><span class="sxs-lookup"><span data-stu-id="700d5-103">IPStore::GetProvParam method</span></span>

<span data-ttu-id="700d5-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="700d5-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="700d5-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="700d5-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="700d5-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="700d5-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="700d5-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="700d5-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="700d5-108">\[這個方法尚未實作。\]</span><span class="sxs-lookup"><span data-stu-id="700d5-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="700d5-109">用於設定指定的參數資訊。</span><span class="sxs-lookup"><span data-stu-id="700d5-109">Intended to set the specified parameter information.</span></span> <span data-ttu-id="700d5-110">但是請注意，它不會執行，而且一律會失敗。</span><span class="sxs-lookup"><span data-stu-id="700d5-110">Note, however, that it is not implemented and will always fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="700d5-111">語法</span><span class="sxs-lookup"><span data-stu-id="700d5-111">Syntax</span></span>


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="700d5-112">參數</span><span class="sxs-lookup"><span data-stu-id="700d5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="700d5-113">*dwParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="700d5-113">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="700d5-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="700d5-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="700d5-115">*pcbData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="700d5-115">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="700d5-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="700d5-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="700d5-117">*ppbData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="700d5-117">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="700d5-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="700d5-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="700d5-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="700d5-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="700d5-120">保留的。</span><span class="sxs-lookup"><span data-stu-id="700d5-120">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="700d5-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="700d5-121">Return value</span></span>

<span data-ttu-id="700d5-122">呼叫這個方法一律會失敗。</span><span class="sxs-lookup"><span data-stu-id="700d5-122">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="700d5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="700d5-123">Requirements</span></span>



| <span data-ttu-id="700d5-124">需求</span><span class="sxs-lookup"><span data-stu-id="700d5-124">Requirement</span></span> | <span data-ttu-id="700d5-125">值</span><span class="sxs-lookup"><span data-stu-id="700d5-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="700d5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="700d5-126">Header</span></span><br/> | <dl> <span data-ttu-id="700d5-127"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="700d5-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="700d5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="700d5-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="700d5-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="700d5-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700d5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="700d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700d5-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="700d5-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
