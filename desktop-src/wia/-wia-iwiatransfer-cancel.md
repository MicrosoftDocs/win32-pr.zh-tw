---
description: 取消目前的傳送作業。
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'IWiaTransfer：： Cancel 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 4764e922498a3c33278555cae37d09c1822959dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511633"
---
# <a name="iwiatransfercancel-method"></a><span data-ttu-id="217ff-103">IWiaTransfer：： Cancel 方法</span><span class="sxs-lookup"><span data-stu-id="217ff-103">IWiaTransfer::Cancel method</span></span>

<span data-ttu-id="217ff-104">取消目前的傳送作業。</span><span class="sxs-lookup"><span data-stu-id="217ff-104">Cancels the current transfer operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="217ff-105">語法</span><span class="sxs-lookup"><span data-stu-id="217ff-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="217ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="217ff-106">Parameters</span></span>

<span data-ttu-id="217ff-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="217ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="217ff-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="217ff-108">Return value</span></span>

<span data-ttu-id="217ff-109">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="217ff-109">Type: **HRESULT**</span></span>

<span data-ttu-id="217ff-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="217ff-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="217ff-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="217ff-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="217ff-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="217ff-112">Requirements</span></span>



| <span data-ttu-id="217ff-113">需求</span><span class="sxs-lookup"><span data-stu-id="217ff-113">Requirement</span></span> | <span data-ttu-id="217ff-114">值</span><span class="sxs-lookup"><span data-stu-id="217ff-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="217ff-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="217ff-115">Minimum supported client</span></span><br/> | <span data-ttu-id="217ff-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="217ff-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="217ff-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="217ff-117">Minimum supported server</span></span><br/> | <span data-ttu-id="217ff-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="217ff-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="217ff-119">標頭</span><span class="sxs-lookup"><span data-stu-id="217ff-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="217ff-120"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="217ff-120"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="217ff-121">Idl</span><span class="sxs-lookup"><span data-stu-id="217ff-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="217ff-122"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="217ff-122"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="217ff-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="217ff-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="217ff-124"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="217ff-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




