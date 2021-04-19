---
description: 抓取離線檔案快取的狀態。
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000932"
---
# <a name="cscquerydatabasestatus-function"></a><span data-ttu-id="60a7c-103">CSCQueryDatabaseStatus 函式</span><span class="sxs-lookup"><span data-stu-id="60a7c-103">CSCQueryDatabaseStatus function</span></span>

<span data-ttu-id="60a7c-104">\[這項功能不受支援，因此不應該使用。\]</span><span class="sxs-lookup"><span data-stu-id="60a7c-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="60a7c-105">抓取離線檔案快取的狀態。</span><span class="sxs-lookup"><span data-stu-id="60a7c-105">Retrieves the status of the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a7c-106">語法</span><span class="sxs-lookup"><span data-stu-id="60a7c-106">Syntax</span></span>


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a><span data-ttu-id="60a7c-107">參數</span><span class="sxs-lookup"><span data-stu-id="60a7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60a7c-108">*pulStatus*</span><span class="sxs-lookup"><span data-stu-id="60a7c-108">*pulStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="60a7c-109">狀態。</span><span class="sxs-lookup"><span data-stu-id="60a7c-109">The status.</span></span> <span data-ttu-id="60a7c-110">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="60a7c-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="60a7c-111">值</span><span class="sxs-lookup"><span data-stu-id="60a7c-111">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="60a7c-112">意義</span><span class="sxs-lookup"><span data-stu-id="60a7c-112">Meaning</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <span data-ttu-id="60a7c-113"><dt>**旗 \_ 標DATABASESTATUS \_ 加密**</dt>的 <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="60a7c-113"><dt>**FLAG\_DATABASESTATUS\_ENCRYPTED**</dt> <dt>0x00000002</dt></span></span> </dl>                                      | <span data-ttu-id="60a7c-114">快取會標示為加密，而且快取中的所有檔案都會加密。</span><span class="sxs-lookup"><span data-stu-id="60a7c-114">The cache is marked for encryption and all files in the cache are encrypted.</span></span><br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <span data-ttu-id="60a7c-115"><dt>**旗 \_ 標DATABASESTATUS \_ 部分 \_ 加密**</dt>的 <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="60a7c-115"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_ENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl>       | <span data-ttu-id="60a7c-116">快取會標示為加密，但快取中的某些檔案並不會加密。</span><span class="sxs-lookup"><span data-stu-id="60a7c-116">The cache is marked for encryption, but some files in the cache are not encrypted.</span></span><br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <span data-ttu-id="60a7c-117"><dt>**旗 \_ 標DATABASESTATUS \_ 部分 \_ 未加密**</dt>的 <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="60a7c-117"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_UNENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="60a7c-118">快取未標示為加密，但尚未解密快取中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="60a7c-118">The cache is not marked for encryption, but not all files in the cache have been decrypted.</span></span><br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <span data-ttu-id="60a7c-119"><dt>**旗 \_ 標DATABASESTATUS \_ 未加密**</dt>的 <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="60a7c-119"><dt>**FLAG\_DATABASESTATUS\_UNENCRYPTED**</dt> <dt>0x00000000</dt></span></span> </dl>                                | <span data-ttu-id="60a7c-120">快取未標示為加密，而且快取中的所有檔案都已解密。</span><span class="sxs-lookup"><span data-stu-id="60a7c-120">The cache is not marked for encryption and all files in the cache have been decrypted.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="60a7c-121">*pulErrors*</span><span class="sxs-lookup"><span data-stu-id="60a7c-121">*pulErrors*</span></span> 
</dt> <dd>

<span data-ttu-id="60a7c-122">如果發生內部資料庫錯誤，此參數為非零值，否則為0。</span><span class="sxs-lookup"><span data-stu-id="60a7c-122">This parameter is a nonzero value if there is an internal database error or 0 otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60a7c-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="60a7c-123">Return value</span></span>

<span data-ttu-id="60a7c-124">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="60a7c-124">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="60a7c-125">備註</span><span class="sxs-lookup"><span data-stu-id="60a7c-125">Remarks</span></span>

<span data-ttu-id="60a7c-126">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="60a7c-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="60a7c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="60a7c-127">Requirements</span></span>



| <span data-ttu-id="60a7c-128">需求</span><span class="sxs-lookup"><span data-stu-id="60a7c-128">Requirement</span></span> | <span data-ttu-id="60a7c-129">值</span><span class="sxs-lookup"><span data-stu-id="60a7c-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60a7c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="60a7c-130">DLL</span></span><br/> | <dl> <span data-ttu-id="60a7c-131"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60a7c-131"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60a7c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60a7c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a7c-133">**CSCIsCSCEnabled**</span><span class="sxs-lookup"><span data-stu-id="60a7c-133">**CSCIsCSCEnabled**</span></span>](csciscscenabled.md)
</dt> </dl>

 

 
