---
description: 建立使用者憑證以用於 NetMeeting 會議。
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995361"
---
# <a name="nmmakecert-function"></a><span data-ttu-id="63b28-103">NmMakeCert 函式</span><span class="sxs-lookup"><span data-stu-id="63b28-103">NmMakeCert function</span></span>

<span data-ttu-id="63b28-104">建立使用者憑證以用於 NetMeeting 會議。</span><span class="sxs-lookup"><span data-stu-id="63b28-104">Creates a user certificate for use with NetMeeting conferencing.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b28-105">語法</span><span class="sxs-lookup"><span data-stu-id="63b28-105">Syntax</span></span>


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="63b28-106">參數</span><span class="sxs-lookup"><span data-stu-id="63b28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b28-107">*szFirstName*</span><span class="sxs-lookup"><span data-stu-id="63b28-107">*szFirstName*</span></span> 
</dt> <dd>

<span data-ttu-id="63b28-108">使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="63b28-108">The user's first name.</span></span>

</dd> <dt>

<span data-ttu-id="63b28-109">*szLastName*</span><span class="sxs-lookup"><span data-stu-id="63b28-109">*szLastName*</span></span> 
</dt> <dd>

<span data-ttu-id="63b28-110">使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="63b28-110">The user's last name.</span></span>

</dd> <dt>

<span data-ttu-id="63b28-111">*szEmailName*</span><span class="sxs-lookup"><span data-stu-id="63b28-111">*szEmailName*</span></span> 
</dt> <dd>

<span data-ttu-id="63b28-112">使用者的電子郵件名稱。</span><span class="sxs-lookup"><span data-stu-id="63b28-112">The user's email name.</span></span>

</dd> <dt>

<span data-ttu-id="63b28-113">*szCity*</span><span class="sxs-lookup"><span data-stu-id="63b28-113">*szCity*</span></span> 
</dt> <dd>

<span data-ttu-id="63b28-114">使用者的城市。</span><span class="sxs-lookup"><span data-stu-id="63b28-114">The user's city.</span></span>

</dd> <dt>

<span data-ttu-id="63b28-115">*szCountry*</span><span class="sxs-lookup"><span data-stu-id="63b28-115">*szCountry*</span></span> 
</dt> <dd>

<span data-ttu-id="63b28-116">使用者的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="63b28-116">The user's country/region.</span></span>

</dd> <dt>

<span data-ttu-id="63b28-117">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="63b28-117">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="63b28-118">指出如何建立憑證的值。</span><span class="sxs-lookup"><span data-stu-id="63b28-118">A value that indicates how the certificate should be created.</span></span> <span data-ttu-id="63b28-119">值可以是下列任何一項。</span><span class="sxs-lookup"><span data-stu-id="63b28-119">Values can be any of the following.</span></span>



| <span data-ttu-id="63b28-120">值</span><span class="sxs-lookup"><span data-stu-id="63b28-120">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="63b28-121">意義</span><span class="sxs-lookup"><span data-stu-id="63b28-121">Meaning</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <span data-ttu-id="63b28-122"><dt>**NMMKCERT \_\_ \_ 僅限 F 清除**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="63b28-122"><dt>**NMMKCERT\_F\_CLEANUP\_ONLY**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="63b28-123">刪除舊憑證，而不建立新的憑證。</span><span class="sxs-lookup"><span data-stu-id="63b28-123">Delete the old certificate without creating a new one.</span></span> <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <span data-ttu-id="63b28-124"><dt>**NMMKCERT \_F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="63b28-124"><dt>**NMMKCERT\_F\_DELETEOLDCERT**</dt> <dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="63b28-125">刪除先前使用此函數建立的舊憑證。</span><span class="sxs-lookup"><span data-stu-id="63b28-125">Delete the old certificate previously created with this function.</span></span> <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <span data-ttu-id="63b28-126"><dt>**NMMKCERT \_F \_ 本機 \_ 電腦**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="63b28-126"><dt>**NMMKCERT\_F\_LOCAL\_MACHINE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="63b28-127">在本機電腦憑證存放區中建立憑證。</span><span class="sxs-lookup"><span data-stu-id="63b28-127">Create the certificate in the local machine certificate store.</span></span> <br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b28-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="63b28-128">Return value</span></span>

<span data-ttu-id="63b28-129">如果函式成功，則傳回1，如果函式失敗，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="63b28-129">Returns 1 if the function succeeds and –1 if the function fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="63b28-130">備註</span><span class="sxs-lookup"><span data-stu-id="63b28-130">Remarks</span></span>

<span data-ttu-id="63b28-131">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="63b28-131">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b28-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="63b28-132">Requirements</span></span>



| <span data-ttu-id="63b28-133">需求</span><span class="sxs-lookup"><span data-stu-id="63b28-133">Requirement</span></span> | <span data-ttu-id="63b28-134">值</span><span class="sxs-lookup"><span data-stu-id="63b28-134">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63b28-135">DLL</span><span class="sxs-lookup"><span data-stu-id="63b28-135">DLL</span></span><br/> | <dl> <span data-ttu-id="63b28-136"><dt>Nmmkcert.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63b28-136"><dt>Nmmkcert.dll</dt></span></span> </dl> |



 

 
