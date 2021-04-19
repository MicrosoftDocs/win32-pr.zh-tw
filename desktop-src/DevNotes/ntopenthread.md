---
description: 使用指定的存取權開啟執行緒物件的控制碼。
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990634"
---
# <a name="ntopenthread-function"></a><span data-ttu-id="7db08-103">NtOpenThread 函式</span><span class="sxs-lookup"><span data-stu-id="7db08-103">NtOpenThread function</span></span>

<span data-ttu-id="7db08-104">\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。</span><span class="sxs-lookup"><span data-stu-id="7db08-104">\[This function may be changed or removed from Windows without further notice.</span></span> <span data-ttu-id="7db08-105">請改用 [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) 函數。\]</span><span class="sxs-lookup"><span data-stu-id="7db08-105">Use the [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function instead.\]</span></span>

<span data-ttu-id="7db08-106">使用指定的存取權開啟執行緒物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7db08-106">Opens a handle to a thread object with the access specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db08-107">語法</span><span class="sxs-lookup"><span data-stu-id="7db08-107">Syntax</span></span>


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a><span data-ttu-id="7db08-108">參數</span><span class="sxs-lookup"><span data-stu-id="7db08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db08-109">*ThreadHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7db08-109">*ThreadHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7db08-110">接收執行緒物件控制碼之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="7db08-110">A pointer to a variable that receives the thread object handle.</span></span>

</dd> <dt>

<span data-ttu-id="7db08-111">*DesiredAccess* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7db08-111">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7db08-112">[**存取 \_ 遮罩**](../secauthz/access-mask-format.md)資料類型，可為執行緒物件提供所需的存取類型。</span><span class="sxs-lookup"><span data-stu-id="7db08-112">An [**ACCESS\_MASK**](../secauthz/access-mask-format.md) data type that provides the desired types of access for the thread object.</span></span>

</dd> <dt>

<span data-ttu-id="7db08-113">*ObjectAttributes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7db08-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7db08-114">[物件 \_ 屬性](https://msdn.microsoft.com/library/aa491657.aspx)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7db08-114">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure.</span></span> <span data-ttu-id="7db08-115">此結構的 **ObjectName** 成員必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="7db08-115">The **ObjectName** member of this structure must be NULL.</span></span>

<span data-ttu-id="7db08-116">**Windows Server 2003 和 WINDOWS XP：** 此結構的 **ObjectName** 成員可指向物件名稱。</span><span class="sxs-lookup"><span data-stu-id="7db08-116">**Windows Server 2003 and Windows XP:** The **ObjectName** member of this structure can point to an object name.</span></span> <span data-ttu-id="7db08-117">如果 **ObjectName** 不是 Null， *ClientId* 參數必須是 null。</span><span class="sxs-lookup"><span data-stu-id="7db08-117">If **ObjectName** is not NULL, the *ClientId* parameter must be NULL.</span></span>

</dd> <dt>

<span data-ttu-id="7db08-118">*ClientId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7db08-118">*ClientId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7db08-119">**用戶端 \_ 識別碼** 結構的指標，識別要開啟其執行緒的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7db08-119">A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span>

<span data-ttu-id="7db08-120">**Windows Server 2003 和 WINDOWS XP：\*\*\*\*用戶端 \_ 識別碼** 結構的指標，識別要開啟其執行緒的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7db08-120">**Windows Server 2003 and Windows XP:** A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span> <span data-ttu-id="7db08-121">此參數可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="7db08-121">This parameter can be NULL.</span></span> <span data-ttu-id="7db08-122">如果這個參數不是 Null，則 *ObjectAttributes* 參數所指向之結構的 **ObjectName** 成員必須是 null。</span><span class="sxs-lookup"><span data-stu-id="7db08-122">If this parameter is not NULL, the **ObjectName** member of the structure pointed to by the *ObjectAttributes* parameter must be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7db08-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="7db08-123">Return value</span></span>

<span data-ttu-id="7db08-124">傳回 **NTSTATUS** 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7db08-124">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="7db08-125">在 WDK 中可用的 Ntstatus 標頭檔中，會列出 **ntstatus** 錯誤碼的表單和重要性，並會在 wdk 檔中說明。</span><span class="sxs-lookup"><span data-stu-id="7db08-125">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db08-126">備註</span><span class="sxs-lookup"><span data-stu-id="7db08-126">Remarks</span></span>

<span data-ttu-id="7db08-127">此函數沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="7db08-127">This function has no associated header file.</span></span> <span data-ttu-id="7db08-128">您可以在 WDK 中取得相關聯的匯入程式庫 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="7db08-128">The associated import library, Ntdll.lib is available in the WDK.</span></span> <span data-ttu-id="7db08-129">您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，動態連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="7db08-129">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="7db08-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7db08-130">Requirements</span></span>



| <span data-ttu-id="7db08-131">需求</span><span class="sxs-lookup"><span data-stu-id="7db08-131">Requirement</span></span> | <span data-ttu-id="7db08-132">值</span><span class="sxs-lookup"><span data-stu-id="7db08-132">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7db08-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7db08-133">DLL</span></span><br/> | <dl> <span data-ttu-id="7db08-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7db08-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
