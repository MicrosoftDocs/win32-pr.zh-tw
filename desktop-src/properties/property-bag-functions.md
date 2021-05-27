---
description: 本節說明一組與 IPropertyBag 物件搭配使用的 Windows helper 函數。
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: 屬性包函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b694c579c76be96b00fa8392344ac59bdc0ce42f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550193"
---
# <a name="property-bag-functions"></a>屬性包函數

本節說明一組與 [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) 物件搭配使用的 Windows helper 函數。



| 主題                                                                       | 目錄                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ 刪除**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | 從屬性包中刪除屬性。<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | 讀取屬性包中屬性的 **BOOL** 資料值。<br/>                                                    |
| [**PSPropertyBag \_ ReadBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | 從屬性包中的屬性讀取 **BSTR** 資料值。<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | 從屬性包中的屬性讀取 **DWORD** 資料值。<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | 從屬性包中的屬性讀取 GUID 資料值。<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | 從屬性包中的屬性讀取 **int** 資料值。<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | 從屬性包中的屬性讀取 **長** 資料值。<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | 抓取儲存在指定屬性包的 [**POINTL**](/previous-versions//dd162807(v=vs.85)) 結構中的屬性座標。<br/>    |
| [**PSPropertyBag \_ ReadPOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | 抓取儲存在指定屬性包的 [**點**](/previous-versions//dd162808(v=vs.85)) 結構中的屬性座標。<br/>    |
| [**PSPropertyBag \_ ReadPropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | 讀取指定屬性包中屬性的屬性索引鍵。<br/>                                                 |
| [**PSPropertyBag \_ ReadRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | 抓取儲存在指定屬性包所包含之屬性中的矩形座標。<br/>              |
| [**PSPropertyBag \_ ReadSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | 讀取屬性包中屬性的 **簡短** 資料值。<br/>                                                   |
| [**PSPropertyBag \_ ReadStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | 讀取屬性包中屬性的 **字串** 資料值。<br/>                                                  |
| [**PSPropertyBag \_ ReadStrAlloc**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | 從屬性包中的屬性讀取 **字串** 資料值，並為讀取的字串配置記憶體。<br/> |
| [**PSPropertyBag \_ ReadStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | 讀取儲存在指定屬性包中所包含之指定屬性的資料流程。<br/>                           |
| [**PSPropertyBag \_ ReadType**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | 讀取屬性包中所儲存之屬性的資料數值型別。<br/>                                      |
| [**PSPropertyBag \_ ReadULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | 從屬性包中的屬性讀取 **ULONGLONG** 資料值。<br/>                                               |
| [**PSPropertyBag \_ ReadUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | 讀取屬性包中未知資料值的指定屬性。<br/>                                                |
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | 設定屬性包中屬性的 **BOOL** 資料值。<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | 從屬性包中的屬性設定 **BSTR** 資料值。<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | 從屬性包中的屬性設定 **DWORD** 資料值。<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | 從屬性包中的屬性設定 GUID 資料值。<br/>                                                       |
| [**PSPropertyBag \_ WriteInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | 從屬性包中的屬性設定 **int** 資料值。<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | 從屬性包中的屬性設定 **LONG** 資料值。<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | 儲存儲存在指定屬性包的 [**POINTL**](/previous-versions//dd162807(v=vs.85)) 結構中的屬性座標。<br/>       |
| [**PSPropertyBag \_ WritePOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | 儲存儲存在指定屬性包的 [**點**](/previous-versions//dd162808(v=vs.85)) 結構中的屬性座標。<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | 設定指定之屬性包中屬性的屬性索引鍵。<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | 儲存儲存在包含于指定屬性包中之屬性的矩形座標。<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | 設定屬性包中屬性的 **簡短** 資料值。<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | 設定屬性包中屬性的 **字串** 資料值。<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | 設定儲存在指定屬性包所包含之指定屬性中的資料流程。<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | 從屬性包中的屬性設定 **ULONGLONG** 資料值。<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | 設定屬性包中未知資料值的指定屬性。<br/>                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PROPVARIANT 和 VARIANT 函式](./functions-propvarutil.md)
</dt> <dt>

[函數](functions.md)
</dt> </dl>

 

 
