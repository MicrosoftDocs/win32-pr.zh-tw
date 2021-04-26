---
description: 指出 WsdCodeGen 是否應該嘗試自動將某些產生的欄位標記為靜態。
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autoStatic 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994925"
---
# <a name="autostatic-element"></a><span data-ttu-id="b6d89-103">autoStatic 元素</span><span class="sxs-lookup"><span data-stu-id="b6d89-103">autoStatic element</span></span>

<span data-ttu-id="b6d89-104">指出 WsdCodeGen 是否應該嘗試自動將某些產生的欄位標記為靜態。</span><span class="sxs-lookup"><span data-stu-id="b6d89-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="b6d89-105">預設會啟用此行為。</span><span class="sxs-lookup"><span data-stu-id="b6d89-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="b6d89-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="b6d89-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="b6d89-107">屬性</span><span class="sxs-lookup"><span data-stu-id="b6d89-107">Attributes</span></span>

<span data-ttu-id="b6d89-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="b6d89-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b6d89-109">子元素</span><span class="sxs-lookup"><span data-stu-id="b6d89-109">Child elements</span></span>

<span data-ttu-id="b6d89-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="b6d89-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b6d89-111">父元素</span><span class="sxs-lookup"><span data-stu-id="b6d89-111">Parent elements</span></span>



| <span data-ttu-id="b6d89-112">元素</span><span class="sxs-lookup"><span data-stu-id="b6d89-112">Element</span></span>                                     | <span data-ttu-id="b6d89-113">描述</span><span class="sxs-lookup"><span data-stu-id="b6d89-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6d89-114">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="b6d89-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="b6d89-115">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="b6d89-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b6d89-116">備註</span><span class="sxs-lookup"><span data-stu-id="b6d89-116">Remarks</span></span>

<span data-ttu-id="b6d89-117">**AutoStatic** 元素不是必要專案，而且可能會在 XML 設定檔中省略。</span><span class="sxs-lookup"><span data-stu-id="b6d89-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="b6d89-118">元素可用來停用產生的欄位標記為靜態，或明確地將某些產生的欄位標記為靜態。</span><span class="sxs-lookup"><span data-stu-id="b6d89-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="b6d89-119">可能的值為 1 (啟用、預設) 和 0 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="b6d89-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="b6d89-120">根據程式碼產生器將程式碼產生器導向至輸出資料的方式而定，啟用 **autoStatic** 可能會造成編譯問題。</span><span class="sxs-lookup"><span data-stu-id="b6d89-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="b6d89-121">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b6d89-121">Element information</span></span>



| <span data-ttu-id="b6d89-122">標籤</span><span class="sxs-lookup"><span data-stu-id="b6d89-122">Label</span></span> | <span data-ttu-id="b6d89-123">值</span><span class="sxs-lookup"><span data-stu-id="b6d89-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b6d89-124">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="b6d89-124">Minimum supported system</span></span><br/> | <span data-ttu-id="b6d89-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6d89-125">Windows Vista</span></span> |
| <span data-ttu-id="b6d89-126">可以是空的</span><span class="sxs-lookup"><span data-stu-id="b6d89-126">Can be empty</span></span>                        | <span data-ttu-id="b6d89-127">是</span><span class="sxs-lookup"><span data-stu-id="b6d89-127">Yes</span></span>           |



 

 




