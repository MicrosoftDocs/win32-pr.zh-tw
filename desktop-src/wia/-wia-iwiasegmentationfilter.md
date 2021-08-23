---
description: IWiaSegmentationFilter 介面會偵測影像資料流程的子領域，並為每個區域建立個別的 IWiaItem2 專案。
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: 'IWiaSegmentationFilter 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 304b5be43aad8afc1730d2a23c170f11f11d319ffc4ae3eb13781efe09da2d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659698"
---
# <a name="iwiasegmentationfilter-interface"></a>IWiaSegmentationFilter 介面

**IWiaSegmentationFilter** 介面會偵測影像資料流程的子領域，並為每個區域建立個別的 [**IWiaItem2**](-wia-iwiaitem2.md)專案。

## <a name="members"></a>成員

**IWiaSegmentationFilter** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaSegmentationFilter** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaSegmentationFilter** 介面具有這些方法。



| 方法                                                             | 描述                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | 決定影像的子領域，這些子領域會在平板玻璃上配置，讓每個子領域都可以取得個別的影像專案。 <br/> |



 

## <a name="remarks"></a>備註

應用程式應該使用 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 來建立分割篩選的新實例。 應用程式通常會在顯示其預覽視窗之前呼叫此函式。

在執行此篩選準則時，請使用 [**IWiaItem2：： CreateChildItem**](-wia-iwiaitem2-createchilditem.md) 來建立子專案。 應用程式應該將 **複製 \_ 父 \_ 屬性 \_ 值** 傳遞給 *ICreationFlags* 參數，以確保在新建立的子系中的屬性（例如影像格式和解析度）相同，如同在父專案中一樣。

分割篩選器必須支援與所用驅動程式搭配使用的所有影像格式。 Microsoft 提供的篩選支援點陣圖 (BMP) 、圖形交換格式 (GIF) 、JPEG、便攜網狀圖形 (PNG) ，以及標記的影像檔案格式 (TIFF) 。

分割篩選器只能用於膠捲和平台掃描器專案。 針對膠捲掃描，掃描器通常會隨附固定的框架，在此情況下，驅動程式會建立子專案，而應用程式不應叫用分割篩選。

**IWiaSegmentationFilter** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。



| IUnknown 方法                                        | 描述                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
