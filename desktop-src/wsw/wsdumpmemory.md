---
title: 'WsDumpMemory 函式 (WebServicesDebug) '
description: 此函數會將所有記憶體配置傾印到主控台。
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- 適用于 Windows 的 WsDumpMemory 函式 Web 服務
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934850"
---
# <a name="wsdumpmemory-function"></a><span data-ttu-id="68666-104">WsDumpMemory 函式</span><span class="sxs-lookup"><span data-stu-id="68666-104">WsDumpMemory function</span></span>

<span data-ttu-id="68666-105">此函數會將所有記憶體配置傾印到主控台。</span><span class="sxs-lookup"><span data-stu-id="68666-105">This function dumps all memory allocations to the console.</span></span>

> [!Note]  
> <span data-ttu-id="68666-106">此函式僅適用于 DEBUG。</span><span class="sxs-lookup"><span data-stu-id="68666-106">This function is for DEBUG ONLY.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="68666-107">語法</span><span class="sxs-lookup"><span data-stu-id="68666-107">Syntax</span></span>


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="68666-108">參數</span><span class="sxs-lookup"><span data-stu-id="68666-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68666-109">*錯誤* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="68666-109">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68666-110">[WS \_ ERROR](ws-error.md)物件的指標，如果函式失敗，則應儲存錯誤的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68666-110">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68666-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="68666-111">Return value</span></span>

<span data-ttu-id="68666-112">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="68666-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68666-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="68666-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68666-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="68666-114">Requirements</span></span>



| <span data-ttu-id="68666-115">需求</span><span class="sxs-lookup"><span data-stu-id="68666-115">Requirement</span></span> | <span data-ttu-id="68666-116">值</span><span class="sxs-lookup"><span data-stu-id="68666-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="68666-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68666-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68666-118">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68666-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                             |
| <span data-ttu-id="68666-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68666-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68666-120">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68666-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="68666-121">標頭</span><span class="sxs-lookup"><span data-stu-id="68666-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68666-122"><dt>WebServicesDebug。h</dt></span><span class="sxs-lookup"><span data-stu-id="68666-122"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





