---
description: 此 API 僅供內部使用，不應在您的程式碼中使用。
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: 'ApiSetQueryApiSetPresence 函式 (Apiquery) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000495"
---
# <a name="apisetqueryapisetpresence-function"></a><span data-ttu-id="e10eb-103">ApiSetQueryApiSetPresence 函式</span><span class="sxs-lookup"><span data-stu-id="e10eb-103">ApiSetQueryApiSetPresence function</span></span>

<span data-ttu-id="e10eb-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e10eb-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e10eb-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e10eb-106">此 API 僅供內部使用，不應在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="e10eb-106">This API is intended for internal use only and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10eb-107">語法</span><span class="sxs-lookup"><span data-stu-id="e10eb-107">Syntax</span></span>


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a><span data-ttu-id="e10eb-108">參數</span><span class="sxs-lookup"><span data-stu-id="e10eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10eb-109">*命名空間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-109">*Namespace* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="e10eb-110">*存在* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-110">*Present* \[out\]</span></span>
<span data-ttu-id="e10eb-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e10eb-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e10eb-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e10eb-112">Requirements</span></span>



| <span data-ttu-id="e10eb-113">需求</span><span class="sxs-lookup"><span data-stu-id="e10eb-113">Requirement</span></span> | <span data-ttu-id="e10eb-114">值</span><span class="sxs-lookup"><span data-stu-id="e10eb-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10eb-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e10eb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e10eb-116">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="e10eb-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e10eb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e10eb-118">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e10eb-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="e10eb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e10eb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e10eb-120"><dt>Apiquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="e10eb-120"><dt>Apiquery.h</dt></span></span> </dl>                                                                                                                 |
| <span data-ttu-id="e10eb-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e10eb-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="e10eb-122"><dt>Api-ms-win-core-apiquery-l1 .lib;</dt><dt>Api-ms-apiquery-l1-1 4.9.0-.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e10eb-122"><dt>Api-ms-win-core-apiquery-l1.lib; </dt> <dt>Api-ms-win-core-apiquery-l1-1-0.lib</dt></span></span> </dl> |
| <span data-ttu-id="e10eb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e10eb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e10eb-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e10eb-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span></span> </dl>                                                                                        |



 

 




