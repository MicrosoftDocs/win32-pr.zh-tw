---
description: IWiaItem2 介面提供與 IWiaItem 介面相同功能的應用程式 (能夠查詢裝置以探索其功能、存取資料傳輸介面和專案屬性，以及控制裝置) 。
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: 'IWiaItem2 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2150b726e6dcdfdeb150de48c78a7a0b2f2ee3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848071"
---
# <a name="iwiaitem2-interface"></a>IWiaItem2 介面

**IWiaItem2** 介面提供與 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)介面相同功能的應用程式 (能夠查詢裝置以探索其功能、存取資料傳輸介面和專案屬性，以及控制裝置) 。 它也提供應用程式動態建立和使用影像處理篩選的能力，而這些篩選器可作為 windows Vista 中提供的 Windows 映像取得 (WIA) 2.0 設備磁碟機的延伸模組。

## <a name="members"></a>成員

**IWiaItem2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaItem2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaItem2** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckExtension**](-wia-iwiaitem2-checkextension.md)                 | 檢查指定的延伸模組是否可在電腦上使用，並可供 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 方法使用。 <br/>                                   |
| [**CreateChildItem**](-wia-iwiaitem2-createchilditem.md)               | 建立新的子專案。 將 **IWiaItem2** 物件新增至裝置的 **IWiaItem2** 樹狀目錄。 <br/>                                                                                                            |
| [**DeleteItem**](-wia-iwiaitem2-deleteitem.md)                         | 從裝置的物件樹狀結構中移除目前的 **IWiaItem2** 物件。 <br/>                                                                                                                          |
| [**DeviceCommand**](-wia-iwiaitem2-devicecommand.md)                   | 發出命令給 WIA 2.0 硬體裝置。 <br/>                                                                                                                                                   |
| [**DeviceDlg**](-wia-iwiaitem2-devicedlg.md)                           | 顯示對話方塊，讓使用者準備取得影像。 <br/>                                                                                                                              |
| [**Diagnostic**](-wia-iwiaitem2-diagnostic.md)                         | 目前不支援。<br/>                                                                                                                                                                          |
| [**EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)                 | 建立列舉值物件，並將其 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) 介面的指標傳回給 WIA 2.0 裝置之 **IWiaItem2** 樹狀目錄中的專案資料夾。 <br/>        |
| [**EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) | 建立用來確定 WIA 2.0 裝置支援的命令和事件的列舉值。 <br/>                                                                                               |
| [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)   | [**IWiaItem2：： EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)方法會建立用來取得已註冊應用程式之事件相關資訊的列舉值。<br/> |
| [**FindItemByName**](-wia-iwiaitem2-finditembyname.md)                 | 使用名稱做為搜尋索引鍵，在專案的子專案樹狀目錄中搜尋。 <br/>                                                                                                                            |
| [**GetExtension**](-wia-iwiaitem2-getextension.md)                     | 取得可能隨附于 WIA 2.0 設備磁碟機的延伸模組介面。 <br/>                                                                                                                      |
| [**GetItemCategory**](-wia-iwiaitem2-getitemcategory.md)               | 取得專案的類別目錄資訊。 <br/>                                                                                                                                                             |
| [**GetItemType**](-wia-iwiaitem2-getitemtype.md)                       | 取得專案的類型資訊。 <br/>                                                                                                                                                                 |
| [**GetParentItem**](-wia-iwiaitem2-getparentitem.md)                   | 取得樹狀結構中表示 WIA 2.0 硬體裝置的父專案。 <br/>                                                                                                                      |
| [**GetPreviewComponent**](-wia-iwiaitem2-getpreviewcomponent.md)       | 取得 WIA 2.0 預覽元件。<br/>                                                                                                                                                               |
| [**GetRootItem**](-wia-iwiaitem2-getrootitem.md)                       | 取得用來表示 WIA 2.0 硬體裝置之專案物件樹狀結構的根專案。 <br/>                                                                                                        |



 

## <a name="remarks"></a>備註

應用程式可以看到的 WIA 2.0 專案樹狀結構與 WIA 2.0 迷你驅動程式所建立和維護的樹狀結構不同。 當迷你驅動程式建立專案樹狀時，WIA 2.0 服務會使用此 WIA 2.0 專案樹狀結構作為指南，以建立可供影像處理應用程式查看的相同複本。 複製之樹狀結構中的專案稱為應用程式專案。 迷你驅動程式所建立之樹狀結構中的專案稱為驅動程式專案。 在 Windows Vista 中，WIA 2.0 專案樹狀結構是內建的 **IWiaItem2** 物件，其中每個物件都會執行 **IWiaItem2** 介面) 。

**IWiaItem2** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。



| IUnknown 方法                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
