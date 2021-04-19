---
description: InetGetAutodial 函式會從登錄傳回自動撥號設定。
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995415"
---
# <a name="inetgetautodial-function"></a><span data-ttu-id="61e5f-103">InetGetAutodial 函式</span><span class="sxs-lookup"><span data-stu-id="61e5f-103">InetGetAutodial function</span></span>

<span data-ttu-id="61e5f-104">\[這項功能不受支援，而且可能會在未來的 Windows 版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="61e5f-104">\[This function is unsupported and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="61e5f-105">\]</span><span class="sxs-lookup"><span data-stu-id="61e5f-105">\]</span></span>

<span data-ttu-id="61e5f-106">**InetGetAutodial** 函式會從登錄傳回自動撥號設定。</span><span class="sxs-lookup"><span data-stu-id="61e5f-106">The **InetGetAutodial** function returns the autodial settings from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e5f-107">語法</span><span class="sxs-lookup"><span data-stu-id="61e5f-107">Syntax</span></span>


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a><span data-ttu-id="61e5f-108">參數</span><span class="sxs-lookup"><span data-stu-id="61e5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e5f-109">*lpfEnable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61e5f-109">*lpfEnable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61e5f-110">指出是否已啟用自動撥號。</span><span class="sxs-lookup"><span data-stu-id="61e5f-110">Indicates whether autodial is enabled.</span></span> <span data-ttu-id="61e5f-111">傳回 **TRUE** 時，表示已啟用自動撥號。</span><span class="sxs-lookup"><span data-stu-id="61e5f-111">A value of **TRUE** upon return indicates autodial is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="61e5f-112">*lpszEntryName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61e5f-112">*lpszEntryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61e5f-113">傳回時，包含為自動撥號設定的電話簿專案名稱。</span><span class="sxs-lookup"><span data-stu-id="61e5f-113">On return, contains the name of the phone book entry that is set for autodial.</span></span>

</dd> <dt>

<span data-ttu-id="61e5f-114">*cbEntryNameSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61e5f-114">*cbEntryNameSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e5f-115">來電者為電話簿專案名稱所配置的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="61e5f-115">Size of the buffer allocated by the caller for the phone book entry name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61e5f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="61e5f-116">Return value</span></span>

<span data-ttu-id="61e5f-117">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="61e5f-117">This function can return one of these values.</span></span>



| <span data-ttu-id="61e5f-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="61e5f-118">Return code</span></span>                                                                                                | <span data-ttu-id="61e5f-119">Description</span><span class="sxs-lookup"><span data-stu-id="61e5f-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61e5f-120"><dt>**錯誤 \_ 成功**</dt></span><span class="sxs-lookup"><span data-stu-id="61e5f-120"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="61e5f-121">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="61e5f-121">The call was successful.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="61e5f-122"><dt>**錯誤 \_ 的 \_ 引數錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="61e5f-122"><dt>**ERROR\_BAD\_ARGUMENTS**</dt></span></span> </dl>       | <span data-ttu-id="61e5f-123">*lpfEnable* 或 *lpszEntryName* 包含 **Null** 指標，或 *cbEntryNameSize* 的值為零。</span><span class="sxs-lookup"><span data-stu-id="61e5f-123">*lpfEnable* or *lpszEntryName* contains a **NULL** pointer, or the value of *cbEntryNameSize* is zero.</span></span><br/>                                         |
| <dl> <span data-ttu-id="61e5f-124"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="61e5f-124"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>  | <span data-ttu-id="61e5f-125">記憶體不足，無法配置內部緩衝區。</span><span class="sxs-lookup"><span data-stu-id="61e5f-125">There was insufficient memory to allocate internal buffers.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="61e5f-126"><dt>**\_緩衝區不足的錯誤 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61e5f-126"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="61e5f-127">*cbEntryNameSize* 並不表示 *lpszEntryName* 所指向的緩衝區夠大，無法接收電話簿專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="61e5f-127">*cbEntryNameSize* does not indicate that the buffer pointed to by *lpszEntryName* is large enough to receive the name of the phone book entry.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61e5f-128">備註</span><span class="sxs-lookup"><span data-stu-id="61e5f-128">Remarks</span></span>

<span data-ttu-id="61e5f-129">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="61e5f-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="61e5f-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="61e5f-130">Requirements</span></span>



| <span data-ttu-id="61e5f-131">需求</span><span class="sxs-lookup"><span data-stu-id="61e5f-131">Requirement</span></span> | <span data-ttu-id="61e5f-132">值</span><span class="sxs-lookup"><span data-stu-id="61e5f-132">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61e5f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="61e5f-133">DLL</span></span><br/> | <dl> <span data-ttu-id="61e5f-134"><dt>Inetcfg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61e5f-134"><dt>Inetcfg.dll</dt></span></span> </dl> |



 

 
