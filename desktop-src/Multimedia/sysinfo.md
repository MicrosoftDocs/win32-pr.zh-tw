---
title: sysinfo 命令
description: Sysinfo 命令會抓取 MCI 系統資訊。 Sysinfo 命令是 MCI 系統命令;它是由 MCI 直接解讀。
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- sysinfo 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966347"
---
# <a name="sysinfo-command"></a>sysinfo 命令

Sysinfo 命令會抓取 MCI 系統資訊。 Sysinfo 命令是 MCI 系統命令;它是由 MCI 直接解讀。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*lpszDeviceID* 
</dt> <dd>

MCI 裝置或裝置類型的識別碼。 如果指定了裝置類型，則它必須是標準的 MCI 裝置類型名稱，如 [**功能**](capability.md) 命令的參考資料中所列。 您可以在 *lpszRequest* 中指定的旗標允許該可能性時，指定 "all"。

</dd> <dt>

*lpszRequest* 
</dt> <dd>

下列其中一個旗標。



| 值                                                                                                                                                                | 意義                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | 傳回登錄或 SYSTEM.INI 檔案中所列的名稱，用來安裝具有指定裝置識別碼的開啟裝置。<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**數量**</dt> </dl>                        | 傳回登錄中列出的 MCI 裝置數目或 *lpszDeviceID* 參數中指定之類型的 SYSTEM.INI 檔案。 此裝置識別碼必須是標準的 MCI 裝置類型名稱。 裝置類型後的任何數位都會被忽略。 針對 *lpszDeviceID* 指定 "all" 會傳回系統中的 MCI 裝置總數。<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**已開啟數量**</dt> </dl>         | 傳回 *lpszDeviceID* 中指定之類型的開啟 MCI 裝置數目。 此裝置識別碼必須是標準的 MCI 裝置類型名稱。 針對 *lpszDeviceID* 指定 "all" 會傳回系統中開啟的 MCI 裝置總數。<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>* * name * index * * *</dt> </dl>                | 傳回 MCI 裝置的名稱。 裝置識別碼必須是標準的 MCI 裝置類型名稱。 *索引* 的範圍是從1到該類型的裝置數目。 如果為 *lpszDeviceID* 指定 "all"， *索引* 的範圍會從1到系統中的裝置總數。<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>**名稱 *索引* 開啟**</dt> </dl> | 傳回開啟的 MCI 裝置名稱。 裝置識別碼必須是標準的 MCI 裝置類型名稱。 *索引* 的範圍是從1到該裝置類型的開啟裝置數目。 如果為 *lpszDeviceID* 指定 "all"， *索引* 的範圍會從1到系統中開啟的裝置總數。<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="examples"></a>範例

下列命令會傳回開啟的波形音訊裝置數目。

``` syntax
sysinfo waveaudio quantity open
```

下列命令會傳回第一個開放式波形音訊裝置 (裝置別名) 的名稱。

``` syntax
sysinfo waveaudio name 1 open
```

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

[**能力**](capability.md)
</dt> </dl>

 

