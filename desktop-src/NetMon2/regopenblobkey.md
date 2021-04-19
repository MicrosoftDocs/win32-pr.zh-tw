---
description: RegOpenBlobKey 函式會在指定的登錄機碼上，抓取儲存的 BLOB。
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: 'RegOpenBlobKey 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997264"
---
# <a name="regopenblobkey-function"></a><span data-ttu-id="55bb9-103">RegOpenBlobKey 函式</span><span class="sxs-lookup"><span data-stu-id="55bb9-103">RegOpenBlobKey function</span></span>

<span data-ttu-id="55bb9-104">**RegOpenBlobKey** 函式會在指定的登錄機碼上，抓取儲存的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="55bb9-104">The **RegOpenBlobKey** function retrieves a BLOB stored at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bb9-105">語法</span><span class="sxs-lookup"><span data-stu-id="55bb9-105">Syntax</span></span>


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="55bb9-106">參數</span><span class="sxs-lookup"><span data-stu-id="55bb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55bb9-107">*hkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55bb9-107">*hkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55bb9-108">包含 BLOB 之登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="55bb9-108">Handle to the registry key that contains the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="55bb9-109">*szBlobName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55bb9-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55bb9-110">識別登錄中指定之 BLOB 的名稱。</span><span class="sxs-lookup"><span data-stu-id="55bb9-110">Name that identifies the given BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="55bb9-111">*phBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55bb9-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55bb9-112">要抓取之 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="55bb9-112">Pointer to the BLOB that is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55bb9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="55bb9-113">Return value</span></span>

<span data-ttu-id="55bb9-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="55bb9-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="55bb9-115">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="55bb9-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bb9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="55bb9-116">Requirements</span></span>



| <span data-ttu-id="55bb9-117">需求</span><span class="sxs-lookup"><span data-stu-id="55bb9-117">Requirement</span></span> | <span data-ttu-id="55bb9-118">值</span><span class="sxs-lookup"><span data-stu-id="55bb9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55bb9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55bb9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55bb9-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55bb9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55bb9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55bb9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55bb9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55bb9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55bb9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="55bb9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bb9-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="55bb9-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="55bb9-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="55bb9-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="55bb9-126"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="55bb9-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="55bb9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="55bb9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55bb9-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55bb9-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55bb9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55bb9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bb9-130">RegCreateBlobKey</span><span class="sxs-lookup"><span data-stu-id="55bb9-130">RegCreateBlobKey</span></span>](regcreateblobkey.md)
</dt> </dl>

 

 




