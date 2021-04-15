---
description: 在目前的進程中註冊 Shell 動態資料交換 (DDE) 服務，通知系統目前的進程希望裝載 DDE 物件。
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973593"
---
# <a name="shellddeinit-function"></a><span data-ttu-id="1ef12-103">ShellDDEInit 函式</span><span class="sxs-lookup"><span data-stu-id="1ef12-103">ShellDDEInit function</span></span>

<span data-ttu-id="1ef12-104">在目前的進程中註冊 Shell 動態資料交換 (DDE) 服務，通知系統目前的進程希望裝載 DDE 物件。</span><span class="sxs-lookup"><span data-stu-id="1ef12-104">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef12-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ef12-105">Syntax</span></span>


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a><span data-ttu-id="1ef12-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ef12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef12-107">*init* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ef12-107">*init* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef12-108">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="1ef12-108">Type: **BOOL**</span></span>

<span data-ttu-id="1ef12-109">**TRUE** 表示將目前的進程註冊為 DDE 主機; **FALSE** 表示將其取消註冊。</span><span class="sxs-lookup"><span data-stu-id="1ef12-109">**TRUE** to register the current process as DDE host; **FALSE** to unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef12-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ef12-110">Return value</span></span>

<span data-ttu-id="1ef12-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1ef12-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef12-112">備註</span><span class="sxs-lookup"><span data-stu-id="1ef12-112">Remarks</span></span>

<span data-ttu-id="1ef12-113">呼叫此函式的進程會作為 Shell，並用來查看以 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ' open ' 動詞開啟之資料夾的內容。</span><span class="sxs-lookup"><span data-stu-id="1ef12-113">The process that calls this function acts as the Shell and is used to view the content of folders opened with the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open' verb.</span></span>

<span data-ttu-id="1ef12-114">此函式沒有相關聯的標頭或程式庫檔案，因此必須由序數值來呼叫。</span><span class="sxs-lookup"><span data-stu-id="1ef12-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="1ef12-115">使用 (Shdocvw.dll) 的 DLL 名稱呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="1ef12-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Shdocvw.dll) to obtain a module handle.</span></span> <span data-ttu-id="1ef12-116">然後使用該模組控制碼呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，並使用函式序號118來取得函式的位址。</span><span class="sxs-lookup"><span data-stu-id="1ef12-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the function ordinal number 118 to get the address of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef12-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ef12-117">Requirements</span></span>



| <span data-ttu-id="1ef12-118">需求</span><span class="sxs-lookup"><span data-stu-id="1ef12-118">Requirement</span></span> | <span data-ttu-id="1ef12-119">值</span><span class="sxs-lookup"><span data-stu-id="1ef12-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef12-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ef12-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef12-121">僅限 windows XP、Windows 2000 Professional \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ef12-121">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ef12-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ef12-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef12-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ef12-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1ef12-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1ef12-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ef12-125"><dt>Shdocvw.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="1ef12-125"><dt>Shdocvw.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
