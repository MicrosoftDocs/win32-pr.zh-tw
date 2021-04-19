---
description: 抓取儲存提供者的介面指標。
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: 'PStoreCreateInstance 函式 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990063"
---
# <a name="pstorecreateinstance-function"></a><span data-ttu-id="c8415-103">PStoreCreateInstance 函式</span><span class="sxs-lookup"><span data-stu-id="c8415-103">PStoreCreateInstance function</span></span>

<span data-ttu-id="c8415-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="c8415-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="c8415-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="c8415-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="c8415-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="c8415-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="c8415-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="c8415-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="c8415-108">\[這項功能可能會在未來的 Windows 版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c8415-108">\[This function may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="c8415-109">使用 **CryptProtectData** 和 **CryptUnprotectData** 函式，而不是此函數。\]</span><span class="sxs-lookup"><span data-stu-id="c8415-109">Use the **CryptProtectData** and **CryptUnprotectData** functions instead of this function.\]</span></span>

<span data-ttu-id="c8415-110">抓取儲存提供者的介面指標。</span><span class="sxs-lookup"><span data-stu-id="c8415-110">Retrieves an interface pointer to a storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8415-111">語法</span><span class="sxs-lookup"><span data-stu-id="c8415-111">Syntax</span></span>


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c8415-112">參數</span><span class="sxs-lookup"><span data-stu-id="c8415-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8415-113">*ppProvider* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8415-113">*ppProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8415-114">儲存提供者之已抓取介面指標的指標。</span><span class="sxs-lookup"><span data-stu-id="c8415-114">A pointer to the retrieved interface pointer for the storage provider.</span></span> <span data-ttu-id="c8415-115">當您使用完介面之後，請呼叫其 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法來遞減其參考計數。</span><span class="sxs-lookup"><span data-stu-id="c8415-115">When you finish using the interface, decrement its reference count by calling its [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="c8415-116">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c8415-116">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-117">*pProviderID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8415-117">*pProviderID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8415-118">識別儲存提供者之 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="c8415-118">A pointer to the **GUID** that identifies the storage provider.</span></span> <span data-ttu-id="c8415-119">如果此參數為 **Null**，則會使用基底儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="c8415-119">If this parameter is **NULL**, then the base storage provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-120">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8415-120">*pReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8415-121">保護必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c8415-121">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c8415-122">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8415-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8415-123">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="c8415-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8415-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8415-124">Return value</span></span>

<span data-ttu-id="c8415-125">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="c8415-125">The return value is an **HRESULT**.</span></span> <span data-ttu-id="c8415-126">值為 **S \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="c8415-126">A value of **S\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8415-127">備註</span><span class="sxs-lookup"><span data-stu-id="c8415-127">Remarks</span></span>

<span data-ttu-id="c8415-128">此函數沒有相關聯的匯入程式庫;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="c8415-128">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8415-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8415-129">Requirements</span></span>



| <span data-ttu-id="c8415-130">需求</span><span class="sxs-lookup"><span data-stu-id="c8415-130">Requirement</span></span> | <span data-ttu-id="c8415-131">值</span><span class="sxs-lookup"><span data-stu-id="c8415-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8415-132">標頭</span><span class="sxs-lookup"><span data-stu-id="c8415-132">Header</span></span><br/> | <dl> <span data-ttu-id="c8415-133"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8415-133"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="c8415-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c8415-134">DLL</span></span><br/>    | <dl> <span data-ttu-id="c8415-135"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8415-135"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8415-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8415-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8415-137">**CryptProtectData**</span><span class="sxs-lookup"><span data-stu-id="c8415-137">**CryptProtectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[<span data-ttu-id="c8415-138">**CryptUnprotectData**</span><span class="sxs-lookup"><span data-stu-id="c8415-138">**CryptUnprotectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
