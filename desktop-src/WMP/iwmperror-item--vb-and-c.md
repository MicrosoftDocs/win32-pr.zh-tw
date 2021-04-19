---
title: 'IWMPError (VB 和 C ) '
description: 專案屬性 (\_ 在 C \ ) 中的 get 專案方法，會在錯誤佇列中的指定索引處取得 IWMPErrorItem 介面。
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- " (VB 和 C ) Windows Media Player 的 IWMPError 專案"
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981365"
---
# <a name="iwmperroritem-vb-and-c"></a><span data-ttu-id="097ec-104">IWMPError (VB 和 c # ) </span><span class="sxs-lookup"><span data-stu-id="097ec-104">IWMPError.Item (VB and C#)</span></span>

<span data-ttu-id="097ec-105">**Item** 屬性 (c # 中的 **get \_ Item** 方法 ) 在錯誤佇列中的指定索引處取得 **IWMPErrorItem** 介面。</span><span class="sxs-lookup"><span data-stu-id="097ec-105">The **Item** property (the **get\_Item** method in C#) gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="097ec-106">參數</span><span class="sxs-lookup"><span data-stu-id="097ec-106">Parameters</span></span>

<span data-ttu-id="097ec-107">*dwIndex*</span><span class="sxs-lookup"><span data-stu-id="097ec-107">*dwIndex*</span></span>

<span data-ttu-id="097ec-108">在錯誤佇列中， **IWMPErrorItem** 介面之以零為基底之索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="097ec-108">A **System.Int32** that is the zero-based index of an **IWMPErrorItem** interface in the error queue.</span></span>

## <a name="property-value"></a><span data-ttu-id="097ec-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="097ec-109">Property Value</span></span>

<span data-ttu-id="097ec-110">**WMPLib IWMPErrorItem** 介面。</span><span class="sxs-lookup"><span data-stu-id="097ec-110">A **WMPLib.IWMPErrorItem** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="097ec-111">備註</span><span class="sxs-lookup"><span data-stu-id="097ec-111">Remarks</span></span>

<span data-ttu-id="097ec-112">Windows Media Player 可能會產生一些錯誤，以回應錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="097ec-112">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="097ec-113">這個屬性會使用索引編號取得佇列中的特定錯誤。</span><span class="sxs-lookup"><span data-stu-id="097ec-113">This property gets a specific error in the queue by using an index number.</span></span> <span data-ttu-id="097ec-114">錯誤佇列的索引編號開頭為零。</span><span class="sxs-lookup"><span data-stu-id="097ec-114">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="097ec-115">如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="097ec-115">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="097ec-116">範例</span><span class="sxs-lookup"><span data-stu-id="097ec-116">Examples</span></span>

<span data-ttu-id="097ec-117">下列範例會使用 **Item** 屬性 (c # 中的 **get \_ Item** 方法 ) 在錯誤事件處理常式中，以抓取和顯示錯誤佇列中最新錯誤的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="097ec-117">The following example uses the **Item** property (the **get\_Item** method in C#) in an Error event handler to retrieve and display information about the most recent error in the error queue.</span></span> <span data-ttu-id="097ec-118">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="097ec-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="097ec-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="097ec-119">Requirements</span></span>



| <span data-ttu-id="097ec-120">需求</span><span class="sxs-lookup"><span data-stu-id="097ec-120">Requirement</span></span> | <span data-ttu-id="097ec-121">值</span><span class="sxs-lookup"><span data-stu-id="097ec-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="097ec-122">版本</span><span class="sxs-lookup"><span data-stu-id="097ec-122">Version</span></span><br/>   | <span data-ttu-id="097ec-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="097ec-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="097ec-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="097ec-124">Namespace</span></span><br/> | <span data-ttu-id="097ec-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="097ec-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="097ec-126">組件</span><span class="sxs-lookup"><span data-stu-id="097ec-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="097ec-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="097ec-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097ec-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="097ec-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097ec-129">**IWMPError 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="097ec-129">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="097ec-130">**IWMPErrorItem 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="097ec-130">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="097ec-131">**IWMPSettings. enableErrorDialogs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="097ec-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





