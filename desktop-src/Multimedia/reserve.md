---
title: reserve 命令
description: Reserve 命令會為裝置實例的工作區配置連續的磁碟空間。 數位影片裝置辨識此命令。
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- 保留命令 Windows 多媒體
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933939"
---
# <a name="reserve-command"></a>reserve 命令

Reserve 命令會為裝置實例的工作區配置連續的磁碟空間。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*
</dt> <dd>

下列一或多個旗標。



| 值           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 *路徑* 中       | 指定磁片磁碟機和目錄路徑 (但不是用來保存記錄資料之暫存檔案的名稱) 。 此檔案的名稱是由裝置所指定。 當裝置關閉時，就會刪除暫存檔案。 如果省略此旗標，則裝置會指定磁碟空間的位置。                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 大小 *持續時間* | 指定要在工作區中保留的大約磁碟空間量。 *Duration* 值是以目前時間格式指定。 裝置會以下列參數為所需磁碟空間的估計值：要求的時間、檔案格式、影片和音訊壓縮演算法，以及作用中的壓縮品質值。 如果 [setvideo](setvideo.md) "record" 為 "off"，則只會保留音訊的空間。 如果 [setaudio](setaudio.md) "record" 為 "off"，則只會保留影片的空間。 如果兩者都是「關閉」，或 *持續時間* 為零，則不會保留任何空間，而且會解除配置任何現有的保留空間。 如果省略此旗標，裝置將會使用裝置定義的預設值。 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

如有需要，後續的 [記錄](record.md) 或 [儲存](save.md) 命令會使用這個命令所保留的空間。 如果工作區包含未儲存的資料，資料就會遺失。 有些裝置不需要保留並予以忽略。 如果在錄製之前未保留磁碟空間，則記錄命令會使用裝置特定的預設旗標來執行隱含的保留。 如果您想要更充分掌控磁片配置的發生時間、控制配置多少空間，以及控制磁碟空間的配置位置，請使用明確的保留命令。 您的應用程式可以使用後續的 reserve 命令變更先前保留磁碟空間的數量和位置。 任何已配置且仍未使用的磁碟空間都不會解除配置，直到儲存任何記錄的資料，或直到裝置實例關閉為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> <dt>

[記錄](record.md)
</dt> <dt>

[儲存](save.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

