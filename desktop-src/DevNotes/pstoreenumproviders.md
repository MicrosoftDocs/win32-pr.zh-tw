---
description: 取得枚舉器物件，這個物件可以用來列舉目前安裝在系統上的受保護儲存提供者。
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: 'PStoreEnumProviders 函式 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996421"
---
# <a name="pstoreenumproviders-function"></a><span data-ttu-id="2bb6f-103">PStoreEnumProviders 函式</span><span class="sxs-lookup"><span data-stu-id="2bb6f-103">PStoreEnumProviders function</span></span>

<span data-ttu-id="2bb6f-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2bb6f-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2bb6f-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2bb6f-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="2bb6f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2bb6f-108">取得枚舉器物件，這個物件可以用來列舉目前安裝在系統上的受保護儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-108">Gets an enumerator object that can be used in turn to enumerate the protected storage providers that are currently installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb6f-109">語法</span><span class="sxs-lookup"><span data-stu-id="2bb6f-109">Syntax</span></span>


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="2bb6f-110">參數</span><span class="sxs-lookup"><span data-stu-id="2bb6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bb6f-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2bb6f-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2bb6f-112">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2bb6f-113">*ppenum*</span><span class="sxs-lookup"><span data-stu-id="2bb6f-113">*ppenum*</span></span> 
</dt> <dd>

<span data-ttu-id="2bb6f-114">指向 [**IEnumPStoreProviders**](ienumpstoreproviders.md) 介面指標的指標，該介面可用來列舉已安裝的提供者。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-114">A pointer to a pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) interface that can be used to enumerate installed providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bb6f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bb6f-115">Return value</span></span>

<span data-ttu-id="2bb6f-116">此函數會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-116">This function returns an **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb6f-117">備註</span><span class="sxs-lookup"><span data-stu-id="2bb6f-117">Remarks</span></span>

<span data-ttu-id="2bb6f-118">受保護的儲存元件具有以提供者為基礎的架構。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-118">The protected storage component has a provider-based architecture.</span></span> <span data-ttu-id="2bb6f-119">使用受保護存放裝置的應用程式可以指定在儲存和抓取其資料時，所要使用的已安裝提供者。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-119">Applications that make use of protected storage can specify which of the installed providers to use when storing and retrieving their data.</span></span>

<span data-ttu-id="2bb6f-120">**PStoreEnumProviders** 函式可用來列舉已安裝的受保護存放裝置提供者。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-120">The **PStoreEnumProviders** function is used to enumerate the installed protected storage providers.</span></span> <span data-ttu-id="2bb6f-121">每個提供者都是以全域唯一識別碼 (GUID) 來識別。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-121">Each provider is identified by a globally unique identifier (GUID).</span></span>

<span data-ttu-id="2bb6f-122">目前為止，只寫入一個受保護的儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-122">Up to this time, only one protected storage provider has ever been written.</span></span> <span data-ttu-id="2bb6f-123">由於受保護的儲存體服務目前已被取代，因此不太可能會產生任何額外的提供者。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-123">Given that the protected storage service is currently deprecated, it is very unlikely that any additional providers will ever be produced.</span></span> <span data-ttu-id="2bb6f-124">因此，此函式不應該用於任何用途。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-124">As a result, this function should not be used for any purpose.</span></span>

<span data-ttu-id="2bb6f-125">此函數沒有相關聯的匯入程式庫;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="2bb6f-125">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb6f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bb6f-126">Requirements</span></span>



| <span data-ttu-id="2bb6f-127">需求</span><span class="sxs-lookup"><span data-stu-id="2bb6f-127">Requirement</span></span> | <span data-ttu-id="2bb6f-128">值</span><span class="sxs-lookup"><span data-stu-id="2bb6f-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb6f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2bb6f-129">Header</span></span><br/> | <dl> <span data-ttu-id="2bb6f-130"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bb6f-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2bb6f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2bb6f-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="2bb6f-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bb6f-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb6f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bb6f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb6f-134">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="2bb6f-134">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
