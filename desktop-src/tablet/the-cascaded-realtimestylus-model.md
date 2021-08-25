---
description: RealTimeStylus 類別的串聯模型總覽。
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: 串聯的 RealTimeStylus 模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf848f1382a8c6a54f58fb6db864ece165c7cff2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467995"
---
# <a name="the-cascaded-realtimestylus-model"></a>串聯的 RealTimeStylus 模型

串聯的 [**realtimestylus**](realtimestylus-class.md) 模型可讓您使用兩個 **RealTimeStylus** 物件，每個物件都在不同的執行緒上執行。 使用此模型，您可以將次要 **realtimestylus** 物件附加至主要的 **realtimestylus** 物件。 次要 **realtimestylus** 物件會附加為主要 **realtimestylus** 物件之非同步外掛程式集合中的唯一非同步外掛程式。

在下列案例中，串聯的 [**RealTimeStylus**](realtimestylus-class.md) 模型可能會很有用。

-   您可以新增一些可能需要計算的工作，但仍需要對 tablet 畫筆的資料流程進行即時存取，例如 multistroke 手勢辨識，以存取次要 [**RealTimeStylus**](realtimestylus-class.md) 物件的同步外掛程式集合。
-   您可以將同步外掛程式的計算負載分散在兩個執行緒上，減少某些 Tablet Pc 上筆跡集合的延遲。

下圖說明 tablet 畫筆資料透過兩個串聯的 [**RealTimeStylus**](realtimestylus-class.md) 物件和其外掛程式集合的流程。

![顯示串聯的 realtimestylus 資料流程的圖例](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

在此圖中，「A」圓圈表示主要和次要 [**realtimestylus**](realtimestylus-class.md) 物件已經處理過的 tablet 畫筆資料，並且已置於次要 **RealTimeStylus** 物件的輸出佇列。 以字母 "B" 表示的 tablet 畫筆資料，已由主要 **realtimestylus** 物件處理並新增至主要 **realtimestylus** 物件的輸出佇列，但尚未傳送至次要 **realtimestylus** 物件。 以字母 "C" 表示主要 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 它會傳送至同步的外掛程式集合，並放在輸出佇列中。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

## <a name="constraints"></a>條件約束

如果您使用預設的 [**realtimestylus**](realtimestylus-class.md)函式，您可以建立只能接受來自另一個 **realtimestylus** 物件之輸入的 **realtimestylus** 物件。

下列清單描述與使用串聯式 [**RealTimeStylus**](realtimestylus-class.md) 模型相關聯的條件約束。

-   只有兩個 [**realtimestylus**](realtimestylus-class.md) 物件可以使用，主要的 **realtimestylus** 物件和次要 **realtimestylus** 物件。
-   主要 [**RealTimeStylus**](realtimestylus-class.md) 物件必須使用使用 **attachedControl** 或 *handle* 參數的函式來建立。 次要 **RealTimeStylus** 物件必須使用無引數的函式來建立。
-   次要 [**realtimestylus**](realtimestylus-class.md) 物件必須是主要 **realtimestylus** 物件之非同步外掛程式集合中的唯一非同步外掛程式。
-   次要 [**realtimestylus**](realtimestylus-class.md) 物件一次只能附加至一個主要的 **realtimestylus** 物件。 如果新增至第二個主要 **realtimestylus** 物件，則 [Add](/previous-versions/ms824814(v=msdn.10)) 方法會擲回例外狀況，而次要 **realtimestylus** 物件不會附加至第二個主要 **realtimestylus** 物件。
-   修改部分次要 [**RealTimeStylus**](realtimestylus-class.md) 物件成員的行為。 下表描述這些成員的修改後行為。

    

    
| 成員 | 行為 | 
|--------|----------|
| <a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a> | 這個方法會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。<br /> 如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，這個方法會傳回預設值。<br /> | 
| <a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a> | 這個方法會引發 <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> 例外狀況。<br /> | 
| <a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a> | 這個方法會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。<br /> 如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，這個方法會傳回空陣列。<br /> | 
| <a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a> | 取得此屬性會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。<br /> 如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，則取得此屬性會傳回預設值。<br /><blockquote>    [!Note]<br />    設定這個屬性會引發 <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> 例外狀況。    </blockquote><br /> | 
| <a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a> | 取得此屬性會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。<br /> 如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，則取得此屬性會傳回預設值。<br /><blockquote>    [!Note]<br />    設定這個屬性會引發 <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> 例外狀況。    </blockquote><br /> | 


    

     

-   當處置子 **realtimestylus** 時，父 [**realtimestylus**](realtimestylus-class.md)物件應該會停止運作。

 

 
