---
description: HTMLValueToUnicode 函式會將 HTML CP \_ UTF8 字串轉換成 Unicode 字串。
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: 'HTMLValueToUnicode 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689711"
---
# <a name="htmlvaluetounicode-function"></a><span data-ttu-id="4e000-103">HTMLValueToUnicode 函式</span><span class="sxs-lookup"><span data-stu-id="4e000-103">HTMLValueToUnicode function</span></span>

<span data-ttu-id="4e000-104">**HTMLValueToUnicode** 函式會將 HTML CP \_ UTF8 字串轉換成 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="4e000-104">The **HTMLValueToUnicode** function converts an HTML CP\_UTF8 string to a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e000-105">語法</span><span class="sxs-lookup"><span data-stu-id="4e000-105">Syntax</span></span>


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="4e000-106">參數</span><span class="sxs-lookup"><span data-stu-id="4e000-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e000-107">*pValue* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4e000-107">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e000-108">在輸入時，指向 MCSVC 所提供之 HTML 字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4e000-108">On input, pointer to the HTML string supplied by the MCSVC.</span></span>

<span data-ttu-id="4e000-109">在輸出時，指向已轉換之 Unicode 字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4e000-109">On output, pointer to the converted Unicode string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e000-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e000-110">Return value</span></span>

<span data-ttu-id="4e000-111">函數會傳回字串的 Unicode 對等專案。</span><span class="sxs-lookup"><span data-stu-id="4e000-111">The function returns the Unicode equivalent of the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e000-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e000-112">Requirements</span></span>



| <span data-ttu-id="4e000-113">需求</span><span class="sxs-lookup"><span data-stu-id="4e000-113">Requirement</span></span> | <span data-ttu-id="4e000-114">值</span><span class="sxs-lookup"><span data-stu-id="4e000-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e000-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e000-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4e000-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e000-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4e000-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e000-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4e000-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e000-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e000-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4e000-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e000-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4e000-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4e000-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e000-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e000-122"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e000-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e000-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4e000-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e000-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e000-124"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




