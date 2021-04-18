---
title: TLSDisconnectFromServer 函式
description: 關閉遠端桌面授權伺服器的開啟控制碼。
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- TLSDisconnectFromServer 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965327"
---
# <a name="tlsdisconnectfromserver-function"></a><span data-ttu-id="94200-104">TLSDisconnectFromServer 函式</span><span class="sxs-lookup"><span data-stu-id="94200-104">TLSDisconnectFromServer function</span></span>

<span data-ttu-id="94200-105">關閉遠端桌面授權伺服器的開啟控制碼。</span><span class="sxs-lookup"><span data-stu-id="94200-105">Closes an open handle to a Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="94200-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="94200-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="94200-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="94200-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="94200-108">語法</span><span class="sxs-lookup"><span data-stu-id="94200-108">Syntax</span></span>


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a><span data-ttu-id="94200-109">參數</span><span class="sxs-lookup"><span data-stu-id="94200-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94200-110">*hHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94200-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94200-111">對 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式的呼叫所開啟的遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="94200-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94200-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="94200-112">Return value</span></span>

<span data-ttu-id="94200-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="94200-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94200-114">備註</span><span class="sxs-lookup"><span data-stu-id="94200-114">Remarks</span></span>

<span data-ttu-id="94200-115">在程式的清除常式中呼叫 **TLSDisconnectFromServer** 函式，以關閉 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式呼叫所開啟的所有伺服器控制碼。</span><span class="sxs-lookup"><span data-stu-id="94200-115">Call the **TLSDisconnectFromServer** function as part of your program's clean-up routine to close all the server handles that are opened by calls to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="94200-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="94200-116">Requirements</span></span>



| <span data-ttu-id="94200-117">需求</span><span class="sxs-lookup"><span data-stu-id="94200-117">Requirement</span></span> | <span data-ttu-id="94200-118">值</span><span class="sxs-lookup"><span data-stu-id="94200-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94200-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94200-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94200-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94200-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94200-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94200-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94200-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94200-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94200-123">DLL</span><span class="sxs-lookup"><span data-stu-id="94200-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94200-124"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94200-124"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94200-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94200-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94200-126">**TLS \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="94200-126">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="94200-127">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="94200-127">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

