---
title: OpenDialog
description: OpenDialog 方法會開啟 [檔案] 對話方塊。
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- OpenDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983258"
---
# <a name="themeopendialog"></a><span data-ttu-id="c1842-104">OpenDialog</span><span class="sxs-lookup"><span data-stu-id="c1842-104">THEME.openDialog</span></span>

<span data-ttu-id="c1842-105">**OpenDialog** 方法會開啟 [檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c1842-105">The **openDialog** method opens a file dialog box.</span></span>

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a><span data-ttu-id="c1842-106">參數</span><span class="sxs-lookup"><span data-stu-id="c1842-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1842-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span><span class="sxs-lookup"><span data-stu-id="c1842-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span></span>
</dt> <dd>

<span data-ttu-id="c1842-108">指定對話方塊類型的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="c1842-108">A **String** that specifies the type of dialog box.</span></span> <span data-ttu-id="c1842-109">必須設定為 "FILE \_ OPEN"。</span><span class="sxs-lookup"><span data-stu-id="c1842-109">Must be set to "FILE\_OPEN".</span></span>

</dd> <dt>

<span data-ttu-id="c1842-110"><span id="parameters"></span><span id="PARAMETERS"></span>*參數*</span><span class="sxs-lookup"><span data-stu-id="c1842-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parameters*</span></span>
</dt> <dd>

<span data-ttu-id="c1842-111">可以用來取得其他資訊的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="c1842-111">A **String** that can be used for additional information.</span></span> <span data-ttu-id="c1842-112">必須設定為 "FILES \_ ALLMEDIA"。</span><span class="sxs-lookup"><span data-stu-id="c1842-112">Must be set to "FILES\_ALLMEDIA".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1842-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1842-113">Return Value</span></span>

<span data-ttu-id="c1842-114">如果使用者按一下 [取消]，這個方法會傳回 **字串** ，其中包含所選取檔案的 URL，或 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="c1842-114">This method returns a **String** containing the URL of the selected file or "" (empty string) if the user clicks cancel.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1842-115">備註</span><span class="sxs-lookup"><span data-stu-id="c1842-115">Remarks</span></span>

<span data-ttu-id="c1842-116">此方法可用於本機硬碟或網路磁碟機機上的檔案。</span><span class="sxs-lookup"><span data-stu-id="c1842-116">This method can be used for files on the local hard drives or on network drives.</span></span>

## <a name="examples"></a><span data-ttu-id="c1842-117">範例</span><span class="sxs-lookup"><span data-stu-id="c1842-117">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="c1842-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1842-118">Requirements</span></span>



| <span data-ttu-id="c1842-119">需求</span><span class="sxs-lookup"><span data-stu-id="c1842-119">Requirement</span></span> | <span data-ttu-id="c1842-120">值</span><span class="sxs-lookup"><span data-stu-id="c1842-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c1842-121">版本</span><span class="sxs-lookup"><span data-stu-id="c1842-121">Version</span></span><br/> | <span data-ttu-id="c1842-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1842-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1842-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1842-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1842-124">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="c1842-124">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





