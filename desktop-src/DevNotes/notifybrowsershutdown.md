---
description: 釋放在流覽 applet 時可能耗用的 JAVA 類別載入器。
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977508"
---
# <a name="notifybrowsershutdown-function"></a><span data-ttu-id="6888a-103">NotifyBrowserShutdown 函式</span><span class="sxs-lookup"><span data-stu-id="6888a-103">NotifyBrowserShutdown function</span></span>

<span data-ttu-id="6888a-104">釋放在流覽 applet 時可能耗用的 JAVA 類別載入器。</span><span class="sxs-lookup"><span data-stu-id="6888a-104">Frees Java class loaders that may have been consumed while browsing the applets.</span></span>

## <a name="syntax"></a><span data-ttu-id="6888a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6888a-105">Syntax</span></span>


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="6888a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6888a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6888a-107">*lpvReserved*</span><span class="sxs-lookup"><span data-stu-id="6888a-107">*lpvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="6888a-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="6888a-108">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6888a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6888a-109">Return value</span></span>

<span data-ttu-id="6888a-110">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6888a-110">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="6888a-111">否則，傳回值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6888a-111">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6888a-112">備註</span><span class="sxs-lookup"><span data-stu-id="6888a-112">Remarks</span></span>

<span data-ttu-id="6888a-113">當瀏覽器視窗的計數在整合式 Web 模式下達到零時，此函式會釋出 JAVA 類別載入器。</span><span class="sxs-lookup"><span data-stu-id="6888a-113">When the count of browser windows reaches zero in integrated Web mode, this function frees the Java class loaders.</span></span> <span data-ttu-id="6888a-114">當使用者再次開始流覽 applet 時，JAVA VM 將會下載最新的類別檔案。</span><span class="sxs-lookup"><span data-stu-id="6888a-114">When the user starts browsing applets again, the Java VM will download the latest class files.</span></span>

<span data-ttu-id="6888a-115">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="6888a-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6888a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6888a-116">Requirements</span></span>



| <span data-ttu-id="6888a-117">需求</span><span class="sxs-lookup"><span data-stu-id="6888a-117">Requirement</span></span> | <span data-ttu-id="6888a-118">值</span><span class="sxs-lookup"><span data-stu-id="6888a-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6888a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6888a-119">DLL</span></span><br/> | <dl> <span data-ttu-id="6888a-120"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6888a-120"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
