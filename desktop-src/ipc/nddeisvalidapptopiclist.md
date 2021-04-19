---
description: 判斷應用程式和主題字串是否 (&\# 0034;AppName \| TopicName&\# 0034; ) 使用適當的語法。
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: 'NDdeIsValidAppTopicList 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996931"
---
# <a name="nddeisvalidapptopiclist-function"></a><span data-ttu-id="4c077-103">NDdeIsValidAppTopicList 函式</span><span class="sxs-lookup"><span data-stu-id="4c077-103">NDdeIsValidAppTopicList function</span></span>

<span data-ttu-id="4c077-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="4c077-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="4c077-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="4c077-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="4c077-106">判斷應用程式和主題字串 ( "*AppName* \| *TopicName*" ) 是否使用適當的語法。</span><span class="sxs-lookup"><span data-stu-id="4c077-106">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c077-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c077-107">Syntax</span></span>


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a><span data-ttu-id="4c077-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c077-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c077-109">*targetTopic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c077-109">*targetTopic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c077-110">要驗證之應用程式和主題字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4c077-110">A pointer to the application and topic string to validate.</span></span> <span data-ttu-id="4c077-111">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4c077-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c077-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c077-112">Return value</span></span>

<span data-ttu-id="4c077-113">如果 *targetTopic* 參數的語法有效，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="4c077-113">If the *targetTopic* parameter has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="4c077-114">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="4c077-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c077-115">備註</span><span class="sxs-lookup"><span data-stu-id="4c077-115">Remarks</span></span>

<span data-ttu-id="4c077-116">[**NDdeShareAdd**](nddeshareadd.md)在建立 DDE 共用時，也會呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="4c077-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c077-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c077-117">Requirements</span></span>



| <span data-ttu-id="4c077-118">需求</span><span class="sxs-lookup"><span data-stu-id="4c077-118">Requirement</span></span> | <span data-ttu-id="4c077-119">值</span><span class="sxs-lookup"><span data-stu-id="4c077-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c077-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c077-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c077-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c077-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4c077-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c077-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c077-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c077-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4c077-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4c077-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c077-125"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c077-125"><dt>Nddeapi.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c077-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c077-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c077-127"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c077-127"><dt>Nddeapi.lib</dt></span></span> </dl>    |
| <span data-ttu-id="4c077-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4c077-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c077-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c077-129"><dt>Nddeapi.dll</dt></span></span> </dl>    |
| <span data-ttu-id="4c077-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4c077-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4c077-131">**NDdeIsValidAppTopicListW** (Unicode) 和 **NDdeIsValidAppTopicListA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4c077-131">**NDdeIsValidAppTopicListW** (Unicode) and **NDdeIsValidAppTopicListA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c077-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c077-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c077-133">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="4c077-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="4c077-134">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="4c077-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="4c077-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="4c077-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




