---
description: RegCreateBlobKey 函式會在指定的登錄機碼上儲存 BLOB。
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: 'RegCreateBlobKey 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975545"
---
# <a name="regcreateblobkey-function"></a><span data-ttu-id="3c0eb-103">RegCreateBlobKey 函式</span><span class="sxs-lookup"><span data-stu-id="3c0eb-103">RegCreateBlobKey function</span></span>

<span data-ttu-id="3c0eb-104">**RegCreateBlobKey** 函式會在指定的登錄機碼上儲存 BLOB。</span><span class="sxs-lookup"><span data-stu-id="3c0eb-104">The **RegCreateBlobKey** function stores a BLOB at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c0eb-105">Syntax</span></span>


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3c0eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c0eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0eb-107">*hkey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c0eb-107">*hkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c0eb-108">將儲存 BLOB 之登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3c0eb-108">Handle to the registry key where the BLOB will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="3c0eb-109">*szBlobName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c0eb-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c0eb-110">代表登錄中 BLOB 的 (應用程式定義) 名稱。</span><span class="sxs-lookup"><span data-stu-id="3c0eb-110">Name (application defined) that represents the BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="3c0eb-111">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c0eb-111">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c0eb-112">儲存之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3c0eb-112">Handle to the BLOB that is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c0eb-113">Return value</span></span>

<span data-ttu-id="3c0eb-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="3c0eb-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3c0eb-115">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="3c0eb-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0eb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c0eb-116">Requirements</span></span>



| <span data-ttu-id="3c0eb-117">需求</span><span class="sxs-lookup"><span data-stu-id="3c0eb-117">Requirement</span></span> | <span data-ttu-id="3c0eb-118">值</span><span class="sxs-lookup"><span data-stu-id="3c0eb-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0eb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c0eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0eb-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0eb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c0eb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c0eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0eb-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c0eb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c0eb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3c0eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c0eb-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3c0eb-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3c0eb-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c0eb-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c0eb-126"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c0eb-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c0eb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3c0eb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c0eb-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c0eb-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c0eb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c0eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0eb-130">RegOpenBlobKey</span><span class="sxs-lookup"><span data-stu-id="3c0eb-130">RegOpenBlobKey</span></span>](regopenblobkey.md)
</dt> </dl>

 

 




