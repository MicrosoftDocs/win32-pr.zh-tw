---
title: TLSConnectToLsServer 函式
description: 開啟指定之遠端桌面授權伺服器的控制碼。
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- TLSConnectToLsServer 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384865"
---
# <a name="tlsconnecttolsserver-function"></a><span data-ttu-id="48335-104">TLSConnectToLsServer 函式</span><span class="sxs-lookup"><span data-stu-id="48335-104">TLSConnectToLsServer function</span></span>

<span data-ttu-id="48335-105">開啟指定之遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="48335-105">Opens a handle to the specified Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="48335-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="48335-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="48335-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="48335-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="48335-108">語法</span><span class="sxs-lookup"><span data-stu-id="48335-108">Syntax</span></span>


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a><span data-ttu-id="48335-109">參數</span><span class="sxs-lookup"><span data-stu-id="48335-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48335-110">*pszLsServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48335-110">*pszLsServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48335-111">以 **null** 結束的字串指標，指定遠端桌面授權伺服器的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="48335-111">Pointer to a **null**-terminated string that specifies the NetBIOS name of the Remote Desktop license server.</span></span> <span data-ttu-id="48335-112">如果這個參數的值為 **Null**，指定的伺服器就是本機電腦。</span><span class="sxs-lookup"><span data-stu-id="48335-112">If the value of this parameter is **NULL**, the specified server is the local computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48335-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="48335-113">Return value</span></span>

<span data-ttu-id="48335-114">如果函式成功，則傳回值是指定之伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="48335-114">If the function succeeds, the return value is a handle to the specified server.</span></span>

<span data-ttu-id="48335-115">如果函式失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="48335-115">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="48335-116">若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="48335-116">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="48335-117">備註</span><span class="sxs-lookup"><span data-stu-id="48335-117">Remarks</span></span>

<span data-ttu-id="48335-118">當您完成使用 **TLSConnectToLsServer** 函式所傳回的控制碼時，請呼叫 [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) 函數來釋放它。</span><span class="sxs-lookup"><span data-stu-id="48335-118">When you have finished using the handle that is returned by the **TLSConnectToLsServer** function, release it by calling the [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="48335-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="48335-119">Requirements</span></span>



| <span data-ttu-id="48335-120">需求</span><span class="sxs-lookup"><span data-stu-id="48335-120">Requirement</span></span> | <span data-ttu-id="48335-121">值</span><span class="sxs-lookup"><span data-stu-id="48335-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48335-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48335-122">Minimum supported client</span></span><br/> | <span data-ttu-id="48335-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48335-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48335-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48335-124">Minimum supported server</span></span><br/> | <span data-ttu-id="48335-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48335-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48335-126">DLL</span><span class="sxs-lookup"><span data-stu-id="48335-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48335-127"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48335-127"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48335-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48335-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48335-129">**TLS \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="48335-129">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="48335-130">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="48335-130">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

