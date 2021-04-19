---
description: 設定指定的參數資訊。
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'IPStore：： SetProvParam 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995914"
---
# <a name="ipstoresetprovparam-method"></a><span data-ttu-id="afddb-103">IPStore：： SetProvParam 方法</span><span class="sxs-lookup"><span data-stu-id="afddb-103">IPStore::SetProvParam method</span></span>

<span data-ttu-id="afddb-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="afddb-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="afddb-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="afddb-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="afddb-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="afddb-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="afddb-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="afddb-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="afddb-108">設定指定的參數資訊。</span><span class="sxs-lookup"><span data-stu-id="afddb-108">Sets the specified parameter information.</span></span>

## <a name="syntax"></a><span data-ttu-id="afddb-109">語法</span><span class="sxs-lookup"><span data-stu-id="afddb-109">Syntax</span></span>


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="afddb-110">參數</span><span class="sxs-lookup"><span data-stu-id="afddb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afddb-111">*dwParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afddb-111">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afddb-112">包含 **PST \_ PP \_ flush \_ PW \_** 快取，以排清使用者密碼快取。</span><span class="sxs-lookup"><span data-stu-id="afddb-112">Contains **PST\_PP\_FLUSH\_PW\_CACHE** to flush the user password cache.</span></span>

</dd> <dt>

<span data-ttu-id="afddb-113">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afddb-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afddb-114">緩衝區中的密碼長度。</span><span class="sxs-lookup"><span data-stu-id="afddb-114">The length of the password in the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="afddb-115">*pbData*</span><span class="sxs-lookup"><span data-stu-id="afddb-115">*pbData*</span></span> 
</dt> <dd>

<span data-ttu-id="afddb-116">包含使用者密碼的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="afddb-116">A pointer to a buffer that contains the user's password.</span></span> <span data-ttu-id="afddb-117">這必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="afddb-117">This must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="afddb-118">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="afddb-118">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="afddb-119">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="afddb-119">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afddb-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="afddb-120">Return value</span></span>

<span data-ttu-id="afddb-121">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="afddb-121">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="afddb-122">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="afddb-122">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="afddb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="afddb-123">Requirements</span></span>



| <span data-ttu-id="afddb-124">需求</span><span class="sxs-lookup"><span data-stu-id="afddb-124">Requirement</span></span> | <span data-ttu-id="afddb-125">值</span><span class="sxs-lookup"><span data-stu-id="afddb-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afddb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="afddb-126">Header</span></span><br/> | <dl> <span data-ttu-id="afddb-127"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="afddb-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="afddb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="afddb-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="afddb-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afddb-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afddb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afddb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afddb-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="afddb-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
