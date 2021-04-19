---
title: IWMPError webHelp 方法
description: WebHelp 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。 |IWMPError webHelp 方法
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- webHelp 方法 Windows Media Player
- webHelp 方法 Windows Media Player，IWMPError 介面
- IWMPError 介面 Windows Media Player，webHelp 方法
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996271"
---
# <a name="iwmperrorwebhelp-method"></a><span data-ttu-id="bf858-107">IWMPError：： webHelp 方法</span><span class="sxs-lookup"><span data-stu-id="bf858-107">IWMPError::webHelp method</span></span>

<span data-ttu-id="bf858-108">**WebHelp** 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。</span><span class="sxs-lookup"><span data-stu-id="bf858-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf858-109">語法</span><span class="sxs-lookup"><span data-stu-id="bf858-109">Syntax</span></span>


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a><span data-ttu-id="bf858-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf858-110">Parameters</span></span>

<span data-ttu-id="bf858-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bf858-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf858-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf858-112">Return value</span></span>

<span data-ttu-id="bf858-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bf858-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf858-114">備註</span><span class="sxs-lookup"><span data-stu-id="bf858-114">Remarks</span></span>

<span data-ttu-id="bf858-115">Web 說明頁面一律包含 Windows Media Player 錯誤的最新和最詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="bf858-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="bf858-116">此方法會自動傳送 Web 說明所需的其他資訊，例如使用的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="bf858-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="bf858-117">若要直接存取 Web 說明頁面，請使用下列錯誤碼和支援中心連結：</span><span class="sxs-lookup"><span data-stu-id="bf858-117">To access the Web Help pages directly, use the following error code and support center links:</span></span>

-   [<span data-ttu-id="bf858-118">Windows Media Player 錯誤碼資訊</span><span class="sxs-lookup"><span data-stu-id="bf858-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="bf858-119">Windows Media Player 解決方案中心</span><span class="sxs-lookup"><span data-stu-id="bf858-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a><span data-ttu-id="bf858-120">範例</span><span class="sxs-lookup"><span data-stu-id="bf858-120">Examples</span></span>

<span data-ttu-id="bf858-121">下列範例會建立一個按鈕，在瀏覽器中啟動 Microsoft Windows Media Player Web 說明頁。</span><span class="sxs-lookup"><span data-stu-id="bf858-121">The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser.</span></span> <span data-ttu-id="bf858-122">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="bf858-122">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="bf858-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf858-123">Requirements</span></span>



| <span data-ttu-id="bf858-124">需求</span><span class="sxs-lookup"><span data-stu-id="bf858-124">Requirement</span></span> | <span data-ttu-id="bf858-125">值</span><span class="sxs-lookup"><span data-stu-id="bf858-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf858-126">版本</span><span class="sxs-lookup"><span data-stu-id="bf858-126">Version</span></span><br/>   | <span data-ttu-id="bf858-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="bf858-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bf858-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf858-128">Namespace</span></span><br/> | <span data-ttu-id="bf858-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bf858-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bf858-130">組件</span><span class="sxs-lookup"><span data-stu-id="bf858-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bf858-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="bf858-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf858-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf858-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf858-133">**IWMPError 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bf858-133">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





