---
description: 釋放金鑰、雜湊或提供者物件。
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: 'SslFreeObject 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848836"
---
# <a name="sslfreeobject-function"></a><span data-ttu-id="d72e3-103">SslFreeObject 函式</span><span class="sxs-lookup"><span data-stu-id="d72e3-103">SslFreeObject function</span></span>

<span data-ttu-id="d72e3-104">**SslFreeObject** 函式會釋放金鑰、雜湊或提供者物件。</span><span class="sxs-lookup"><span data-stu-id="d72e3-104">The **SslFreeObject** function frees a key, hash, or provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d72e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="d72e3-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d72e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="d72e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72e3-107">*hObject* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d72e3-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d72e3-108">要釋放的物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="d72e3-108">The handle of the object to free.</span></span>

</dd> <dt>

<span data-ttu-id="d72e3-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d72e3-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d72e3-110">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="d72e3-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d72e3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d72e3-111">Return value</span></span>

<span data-ttu-id="d72e3-112">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d72e3-112">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="d72e3-113">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="d72e3-113">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="d72e3-114">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="d72e3-114">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="d72e3-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d72e3-115">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="d72e3-116">Description</span><span class="sxs-lookup"><span data-stu-id="d72e3-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d72e3-117">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="d72e3-117"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="d72e3-118">內部控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="d72e3-118">An internal handle is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="d72e3-119"><dt>**狀態 \_不正確 \_ 控制碼**</dt> <dt>0xC0000008L</dt></span><span class="sxs-lookup"><span data-stu-id="d72e3-119"><dt>**STATUS\_INVALID\_HANDLE**</dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="d72e3-120">提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="d72e3-120">The provided handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d72e3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d72e3-121">Requirements</span></span>



| <span data-ttu-id="d72e3-122">需求</span><span class="sxs-lookup"><span data-stu-id="d72e3-122">Requirement</span></span> | <span data-ttu-id="d72e3-123">值</span><span class="sxs-lookup"><span data-stu-id="d72e3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d72e3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d72e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d72e3-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d72e3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d72e3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d72e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d72e3-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d72e3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d72e3-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d72e3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d72e3-129"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="d72e3-129"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="d72e3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d72e3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d72e3-131"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d72e3-131"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




