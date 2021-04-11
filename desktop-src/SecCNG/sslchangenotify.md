---
description: 未執行且無法使用。
ms.assetid: b41ba894-5cee-458d-935f-e89363925968
title: 'SslChangeNotify 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslChangeNotify
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5539ef2529a4f3af86d34ae0e9d44cd31a8f4289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115177"
---
# <a name="sslchangenotify-function"></a><span data-ttu-id="649ed-103">SslChangeNotify 函式</span><span class="sxs-lookup"><span data-stu-id="649ed-103">SslChangeNotify function</span></span>

<span data-ttu-id="649ed-104">**SslChangeNotify** 函式不會執行，而且無法使用。</span><span class="sxs-lookup"><span data-stu-id="649ed-104">The **SslChangeNotify** function is not implemented and cannot be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="649ed-105">語法</span><span class="sxs-lookup"><span data-stu-id="649ed-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslChangeNotify(
  _In_ HANDLE hEvent,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="649ed-106">參數</span><span class="sxs-lookup"><span data-stu-id="649ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="649ed-107">*hEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="649ed-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649ed-108">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="649ed-108">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="649ed-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="649ed-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649ed-110">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="649ed-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="649ed-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="649ed-111">Return value</span></span>

<span data-ttu-id="649ed-112">傳回 **\_ 不 \_ 支援的上限**。</span><span class="sxs-lookup"><span data-stu-id="649ed-112">Returns **NTE\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="649ed-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="649ed-113">Requirements</span></span>



| <span data-ttu-id="649ed-114">需求</span><span class="sxs-lookup"><span data-stu-id="649ed-114">Requirement</span></span> | <span data-ttu-id="649ed-115">值</span><span class="sxs-lookup"><span data-stu-id="649ed-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="649ed-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="649ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="649ed-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="649ed-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="649ed-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="649ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="649ed-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="649ed-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="649ed-120">標頭</span><span class="sxs-lookup"><span data-stu-id="649ed-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="649ed-121"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="649ed-121"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="649ed-122">DLL</span><span class="sxs-lookup"><span data-stu-id="649ed-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="649ed-123"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="649ed-123"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




