---
title: 'IWMPSettings. isAvailable (VB 和 C ) '
description: IsAvailable 屬性 (\_ 在 C \ ) 的 get isAvailable 方法會取得值，這個值會指出是否可以執行指定的動作。
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. isAvailable (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991560"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a><span data-ttu-id="edef6-104">IWMPSettings. isAvailable (VB 和 c # ) </span><span class="sxs-lookup"><span data-stu-id="edef6-104">IWMPSettings.isAvailable (VB and C#)</span></span>

<span data-ttu-id="edef6-105">**IsAvailable** 屬性 (c # 中的 **get \_ isAvailable** 方法 ) 取得值，指出是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="edef6-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="edef6-106">參數</span><span class="sxs-lookup"><span data-stu-id="edef6-106">Parameters</span></span>

<span data-ttu-id="edef6-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="edef6-107">*bstrItem*</span></span>

<span data-ttu-id="edef6-108">**System.string** ，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="edef6-108">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="edef6-109">值</span><span class="sxs-lookup"><span data-stu-id="edef6-109">Value</span></span>              | <span data-ttu-id="edef6-110">描述</span><span class="sxs-lookup"><span data-stu-id="edef6-110">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edef6-111">AutoStart</span><span class="sxs-lookup"><span data-stu-id="edef6-111">AutoStart</span></span>          | <span data-ttu-id="edef6-112">探索是否可以設定 [自動啟動] 屬性，以指定 Windows Media Player 自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="edef6-112">Discovers whether the autoStart property can be set to specify that Windows Media Player starts playback automatically.</span></span> |
| <span data-ttu-id="edef6-113">餘額</span><span class="sxs-lookup"><span data-stu-id="edef6-113">Balance</span></span>            | <span data-ttu-id="edef6-114">探索是否可以使用餘額屬性來設定身歷聲平衡。</span><span class="sxs-lookup"><span data-stu-id="edef6-114">Discovers whether the balance property can be used to set the stereo balance.</span></span>                                           |
| <span data-ttu-id="edef6-115">BaseURL</span><span class="sxs-lookup"><span data-stu-id="edef6-115">BaseURL</span></span>            | <span data-ttu-id="edef6-116">探索是否可以設定 baseURL 屬性來指定基底 URL。</span><span class="sxs-lookup"><span data-stu-id="edef6-116">Discovers whether the baseURL property can be set to specify a base URL.</span></span>                                                |
| <span data-ttu-id="edef6-117">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="edef6-117">DefaultFrame</span></span>       | <span data-ttu-id="edef6-118">探索是否可以設定 defaultFrame 屬性來指定預設框架。</span><span class="sxs-lookup"><span data-stu-id="edef6-118">Discovers whether the defaultFrame property can be set to specify the default frame.</span></span>                                    |
| <span data-ttu-id="edef6-119">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="edef6-119">EnableErrorDialogs</span></span> | <span data-ttu-id="edef6-120">探索是否可以將 enableErrorDialogs 屬性設定為啟用或停用顯示錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="edef6-120">Discovers whether the enableErrorDialogs property can be set to enable or disable displaying error dialog boxes.</span></span>        |
| <span data-ttu-id="edef6-121">GetMode</span><span class="sxs-lookup"><span data-stu-id="edef6-121">GetMode</span></span>            | <span data-ttu-id="edef6-122">探索是否可以使用 getMode 方法來取得目前的迴圈或隨機模式。</span><span class="sxs-lookup"><span data-stu-id="edef6-122">Discovers whether the getMode method can be used to retrieve the current loop or shuffle mode.</span></span>                          |
| <span data-ttu-id="edef6-123">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="edef6-123">InvokeURLs</span></span>         | <span data-ttu-id="edef6-124">探索是否可以設定 invokeURLs 屬性，以指定 URL 事件是否應啟動網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="edef6-124">Discovers whether the invokeURLs property can be set to specify whether URL events should launch a Web browser.</span></span>         |
| <span data-ttu-id="edef6-125">Mute</span><span class="sxs-lookup"><span data-stu-id="edef6-125">Mute</span></span>               | <span data-ttu-id="edef6-126">探索是否可以設定 [靜音] 屬性，以指定音訊輸出為開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="edef6-126">Discovers whether the mute property can be set to specify whether the audio output is on or off.</span></span>                        |
| <span data-ttu-id="edef6-127">PlayCount</span><span class="sxs-lookup"><span data-stu-id="edef6-127">PlayCount</span></span>          | <span data-ttu-id="edef6-128">探索是否可以設定 playCount 屬性，以指定媒體專案將播放的次數。</span><span class="sxs-lookup"><span data-stu-id="edef6-128">Discovers whether the playCount property can be set to specify the number times a media item will play.</span></span>                 |
| <span data-ttu-id="edef6-129">費率</span><span class="sxs-lookup"><span data-stu-id="edef6-129">Rate</span></span>               | <span data-ttu-id="edef6-130">探索是否可以設定 rate 屬性來控制播放速率。</span><span class="sxs-lookup"><span data-stu-id="edef6-130">Discovers whether the rate property can be set to control the playback rate.</span></span>                                            |
| <span data-ttu-id="edef6-131">SetMode</span><span class="sxs-lookup"><span data-stu-id="edef6-131">SetMode</span></span>            | <span data-ttu-id="edef6-132">探索 setMode 方法是否可以用來指定目前的迴圈或隨機模式。</span><span class="sxs-lookup"><span data-stu-id="edef6-132">Discovers whether the setMode method can be used to specify the current loop or shuffle mode.</span></span>                           |
| <span data-ttu-id="edef6-133">磁碟區</span><span class="sxs-lookup"><span data-stu-id="edef6-133">Volume</span></span>             | <span data-ttu-id="edef6-134">探索是否可以設定磁片區屬性來指定音訊卷。</span><span class="sxs-lookup"><span data-stu-id="edef6-134">Discovers whether the volume property can be set to specify the audio volume.</span></span>                                           |



 

## <a name="property-value"></a><span data-ttu-id="edef6-135">屬性值</span><span class="sxs-lookup"><span data-stu-id="edef6-135">Property Value</span></span>

<span data-ttu-id="edef6-136">System.string **值，** 指出是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="edef6-136">A **System.Boolean** value indicating whether the specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="edef6-137">備註</span><span class="sxs-lookup"><span data-stu-id="edef6-137">Remarks</span></span>

<span data-ttu-id="edef6-138">**IWMPSettings. isIdentical** 是 Visual Basic 中接受參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="edef6-138">**IWMPSettings.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="edef6-139">在 c # 中，它稱為 **IWMPSettings. get \_ isIdentical** 方法。</span><span class="sxs-lookup"><span data-stu-id="edef6-139">In C# it is referred to as the **IWMPSettings.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="edef6-140">範例</span><span class="sxs-lookup"><span data-stu-id="edef6-140">Examples</span></span>

<span data-ttu-id="edef6-141">下列範例會使用 **isAvailable** 屬性來測試每個 **IWMPSettings** 屬性， (c # ) 中的 **get \_ isAvailable** 方法。</span><span class="sxs-lookup"><span data-stu-id="edef6-141">The following example tests each of the **IWMPSettings** properties using the **isAvailable** property (the **get\_isAvailable** method in C#).</span></span> <span data-ttu-id="edef6-142">屬性名稱和每個測試的結果都會顯示在多行文字方塊中。</span><span class="sxs-lookup"><span data-stu-id="edef6-142">The property name and the result of each test are displayed in a multi-line text box.</span></span> <span data-ttu-id="edef6-143">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="edef6-143">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a><span data-ttu-id="edef6-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="edef6-144">Requirements</span></span>



| <span data-ttu-id="edef6-145">需求</span><span class="sxs-lookup"><span data-stu-id="edef6-145">Requirement</span></span> | <span data-ttu-id="edef6-146">值</span><span class="sxs-lookup"><span data-stu-id="edef6-146">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edef6-147">版本</span><span class="sxs-lookup"><span data-stu-id="edef6-147">Version</span></span><br/>   | <span data-ttu-id="edef6-148">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="edef6-148">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="edef6-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="edef6-149">Namespace</span></span><br/> | <span data-ttu-id="edef6-150">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="edef6-150">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="edef6-151">組件</span><span class="sxs-lookup"><span data-stu-id="edef6-151">Assembly</span></span><br/>  | <dl> <span data-ttu-id="edef6-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="edef6-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edef6-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edef6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edef6-154">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-154">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-155">**IWMPSettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-155">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-156">**IWMPSettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-156">**IWMPSettings.balance (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-157">**IWMPSettings. baseURL (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-157">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-158">**IWMPSettings. defaultFrame (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-158">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-159">**IWMPSettings. enableErrorDialogs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-159">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-160">**IWMPSettings. getMode (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-160">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-161">**IWMPSettings. invokeURLs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-161">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-162">**IWMPSettings (VB 和 c # ) 靜音**</span><span class="sxs-lookup"><span data-stu-id="edef6-162">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-163">**IWMPSettings. playCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-163">**IWMPSettings.playCount (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-164">**IWMPSettings (VB 和 c # 的速率 )**</span><span class="sxs-lookup"><span data-stu-id="edef6-164">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-165">**IWMPSettings. setMode (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-165">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edef6-166">**IWMPSettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="edef6-166">**IWMPSettings.volume (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





