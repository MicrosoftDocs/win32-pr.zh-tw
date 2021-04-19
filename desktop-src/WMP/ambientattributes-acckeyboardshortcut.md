---
title: AmbientAttributes.accKeyboardShortcut
description: AccKeyboardShortcut 屬性會指定或抓取任何元素的鍵盤快速鍵描述。
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes. accKeyboardShortcut Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982985"
---
# <a name="ambientattributesacckeyboardshortcut"></a><span data-ttu-id="408b4-104">AmbientAttributes.accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="408b4-104">AmbientAttributes.accKeyboardShortcut</span></span>

<span data-ttu-id="408b4-105">**AccKeyboardShortcut** 屬性會指定或抓取任何元素的鍵盤快速鍵描述。</span><span class="sxs-lookup"><span data-stu-id="408b4-105">The **accKeyboardShortcut** attribute specifies or retrieves a keyboard shortcut description for any element.</span></span>

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a><span data-ttu-id="408b4-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="408b4-106">Possible Values</span></span>

<span data-ttu-id="408b4-107">此屬性是讀取/寫入 **字串** ，其預設值為 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="408b4-107">This attribute is a read/write **String** with a default value of "" (empty string).</span></span> <span data-ttu-id="408b4-108">若為 **BUTTON** 元素，此屬性的預設值為 "空格鍵或 Enter"。</span><span class="sxs-lookup"><span data-stu-id="408b4-108">For the **BUTTON** element, this attribute has a default value of "Spacebar or Enter".</span></span> <span data-ttu-id="408b4-109">若為 **滑杆** 元素，預設值為「向右/向上箭號，可增加、向左/向下箭號以減少」。</span><span class="sxs-lookup"><span data-stu-id="408b4-109">For the **SLIDER** element, the default value is "Right/Up Arrow to increase, Left/Down Arrow to decrease".</span></span>

## <a name="remarks"></a><span data-ttu-id="408b4-110">備註</span><span class="sxs-lookup"><span data-stu-id="408b4-110">Remarks</span></span>

<span data-ttu-id="408b4-111">這個屬性會用於協助工具用途。</span><span class="sxs-lookup"><span data-stu-id="408b4-111">This attribute is used for accessibility purposes.</span></span> <span data-ttu-id="408b4-112">它允許讀取器程式大聲讀出任何專案的鍵盤快速鍵描述。</span><span class="sxs-lookup"><span data-stu-id="408b4-112">It allows a description of the keyboard shortcut for any element to be read aloud by a reader program.</span></span> <span data-ttu-id="408b4-113">這個屬性不會設定快捷方式。</span><span class="sxs-lookup"><span data-stu-id="408b4-113">This attribute does not set the shortcut.</span></span> <span data-ttu-id="408b4-114">腳本處理常式必須執行該工作。</span><span class="sxs-lookup"><span data-stu-id="408b4-114">The scripter must do that work.</span></span>

<span data-ttu-id="408b4-115">這個屬性也適用于按鈕群組控制項內的按鈕元素。</span><span class="sxs-lookup"><span data-stu-id="408b4-115">This attribute also applies to button elements inside the button group control.</span></span>

## <a name="requirements"></a><span data-ttu-id="408b4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="408b4-116">Requirements</span></span>



| <span data-ttu-id="408b4-117">需求</span><span class="sxs-lookup"><span data-stu-id="408b4-117">Requirement</span></span> | <span data-ttu-id="408b4-118">值</span><span class="sxs-lookup"><span data-stu-id="408b4-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="408b4-119">版本</span><span class="sxs-lookup"><span data-stu-id="408b4-119">Version</span></span><br/> | <span data-ttu-id="408b4-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="408b4-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="408b4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="408b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="408b4-122">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="408b4-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





