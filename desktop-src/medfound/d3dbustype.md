---
description: 指定圖形介面卡所使用的 i/o 匯流排類型。
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: 'D3DBUSTYPE 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973987"
---
# <a name="d3dbustype-enumeration"></a>D3DBUSTYPE 列舉

指定圖形介面卡所使用的 i/o 匯流排類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ 其他**
</dt> <dd>

指出此處所列類型以外的匯流排類型。

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
</dt> <dd>

PCI 匯流排。

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**
</dt> <dd>

PCI X 匯流排。

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**
</dt> <dd>

PCI Express 匯流排。

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

高速圖形連接埠 (AGP) 匯流排。

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_ \_ 在晶片內部 \_ D3DBUSIMPL 修飾詞 \_**
</dt> <dd>

圖形介面卡的執行是在主機板晶片的北方 bridge 中。 此旗標表示資料永遠不會超出展開匯流排 (例如 PCI 或 AGP) 從主儲存體傳輸到圖形介面卡時。

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL \_ 修飾 \_ 詞 \_ 在 \_ \_ 主機板 \_ 到 \_ 晶片的軌跡**
</dt> <dd>

指出圖形介面卡已透過板上的曲目，連接至主機板晶片的北方橋接器，而所有圖形介面卡的晶片都會焊接到主機板上。 此旗標表示資料永遠不會超出展開匯流排 (例如 PCI 或 AGP) 從主儲存體傳輸到圖形介面卡時。

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**將 D3DBUSIMPL 修飾詞從 \_ \_ \_ \_ \_ 主機板 \_ 到 \_ 通訊端的追蹤**
</dt> <dd>

圖形介面卡會透過在主機板上進行追蹤，連接至主機板晶片的北方橋接器，而所有圖形介面卡的晶片都會透過通訊端連接至主機板。

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL \_ 修飾詞 \_ 子 \_ 面板 \_ 連接器**
</dt> <dd>

圖形介面卡透過 daughterboard 連接器連線至主機板。

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ \_ \_ \_ \_ NUAE 內的 \_ D3DBUSIMPL 修飾詞子面板連接器**
</dt> <dd>

圖形介面卡透過 daughterboard 連接器連線至主機板，而圖形介面卡位於無法存取使用者的主機殼內。

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL \_ 修飾詞 \_ 非 \_ 標準**
</dt> <dd>

其中一個 D3DBUSIMPL \_ 修飾詞 \_ 修飾詞 \_ Xxx 旗標已設定。

</dd> </dl>

## <a name="remarks"></a>備註

最多可以設定三個旗標。 範圍從0x00 到0x04 的旗標 (**D3DBUSTYPE \_ Xxx**) 提供基本的匯流排類型。 範圍0x10000 到 0x50000 (**D3DBUSIMPL \_ 修飾詞 \_ Xxx** 的旗標，) 修改基本描述。 驅動程式會設定一個匯流排類型旗標，而且可以設定零或一個修飾詞旗標。 如果驅動程式設定了修飾詞旗標，也會設定 **D3DBUSIMPL \_ 修飾詞 \_ 非 \_ 標準** 旗標。 旗標會與位 **or** 合併。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>D3d9types (包含 D3d9) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片列舉](direct3d-video-enumerations.md)
</dt> </dl>

 

 




