---
description: 傳回存放裝置提供者的資訊。
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'IPStore：： GetInfo 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986576"
---
# <a name="ipstoregetinfo-method"></a><span data-ttu-id="55923-103">IPStore：： GetInfo 方法</span><span class="sxs-lookup"><span data-stu-id="55923-103">IPStore::GetInfo method</span></span>

<span data-ttu-id="55923-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="55923-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="55923-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="55923-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="55923-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="55923-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="55923-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="55923-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="55923-108">傳回存放裝置提供者的資訊。</span><span class="sxs-lookup"><span data-stu-id="55923-108">Returns information on the storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="55923-109">語法</span><span class="sxs-lookup"><span data-stu-id="55923-109">Syntax</span></span>


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="55923-110">參數</span><span class="sxs-lookup"><span data-stu-id="55923-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55923-111">*ppProperties* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55923-111">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55923-112">**PPST \_ PROVIDERINFO** 結構的指標，其中包含儲存提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="55923-112">A pointer to a **PPST\_PROVIDERINFO** structure that contains information about the storage provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55923-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="55923-113">Return value</span></span>

<span data-ttu-id="55923-114">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="55923-114">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="55923-115">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="55923-115">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="55923-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="55923-116">Requirements</span></span>



| <span data-ttu-id="55923-117">需求</span><span class="sxs-lookup"><span data-stu-id="55923-117">Requirement</span></span> | <span data-ttu-id="55923-118">值</span><span class="sxs-lookup"><span data-stu-id="55923-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55923-119">標頭</span><span class="sxs-lookup"><span data-stu-id="55923-119">Header</span></span><br/> | <dl> <span data-ttu-id="55923-120"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="55923-120"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="55923-121">DLL</span><span class="sxs-lookup"><span data-stu-id="55923-121">DLL</span></span><br/>    | <dl> <span data-ttu-id="55923-122"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55923-122"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55923-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55923-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55923-124">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="55923-124">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
