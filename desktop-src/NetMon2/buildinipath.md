---
description: BuildINIPath 函式會傳回 INI 檔案的完整路徑，該檔案會對應到您輸入的資訊。
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: 'BuildINIPath 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984575"
---
# <a name="buildinipath-function"></a><span data-ttu-id="1d66a-103">BuildINIPath 函式</span><span class="sxs-lookup"><span data-stu-id="1d66a-103">BuildINIPath function</span></span>

<span data-ttu-id="1d66a-104">**BuildINIPath** 函式會傳回 INI 檔案的完整路徑，該檔案會對應到您輸入的資訊。</span><span class="sxs-lookup"><span data-stu-id="1d66a-104">The **BuildINIPath** function returns a fully qualified path to an INI file that corresponds to information you enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d66a-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d66a-105">Syntax</span></span>


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a><span data-ttu-id="1d66a-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d66a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d66a-107">*FullPath*</span><span class="sxs-lookup"><span data-stu-id="1d66a-107">*FullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="1d66a-108">接收完整 INI 檔案名的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1d66a-108">Buffer that receives the fully qualified INI file name.</span></span>

</dd> <dt>

<span data-ttu-id="1d66a-109">*IniFileName*</span><span class="sxs-lookup"><span data-stu-id="1d66a-109">*IniFileName*</span></span> 
</dt> <dd>

<span data-ttu-id="1d66a-110">INI 檔案名 (檔案名減去副檔名) 的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="1d66a-110">Name of the INI file (the full file name minus the filename extension).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d66a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d66a-111">Return value</span></span>

<span data-ttu-id="1d66a-112">如果函式成功，則傳回值會是完整 INI 檔案名的指標。</span><span class="sxs-lookup"><span data-stu-id="1d66a-112">If the function is successful, the return value is a pointer to the fully qualified INI file name.</span></span>

<span data-ttu-id="1d66a-113">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1d66a-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d66a-114">備註</span><span class="sxs-lookup"><span data-stu-id="1d66a-114">Remarks</span></span>

<span data-ttu-id="1d66a-115">此函式傳回的路徑是與您輸入的資訊對應之 INI 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1d66a-115">The path that this function returns is a fully qualified path to an INI file that corresponds to information you enter.</span></span> <span data-ttu-id="1d66a-116">例如，如果您輸入 XNS 或 TCP，函數會分別產生 Xns.ini 或 Tcp.ini 的路徑。</span><span class="sxs-lookup"><span data-stu-id="1d66a-116">For example, if you enter XNS or TCP, the function generates a path to Xns.ini or Tcp.ini, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d66a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d66a-117">Requirements</span></span>



| <span data-ttu-id="1d66a-118">需求</span><span class="sxs-lookup"><span data-stu-id="1d66a-118">Requirement</span></span> | <span data-ttu-id="1d66a-119">值</span><span class="sxs-lookup"><span data-stu-id="1d66a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d66a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d66a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d66a-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d66a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1d66a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d66a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d66a-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d66a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d66a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1d66a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d66a-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1d66a-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d66a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d66a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d66a-127"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d66a-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="1d66a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1d66a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d66a-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d66a-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




