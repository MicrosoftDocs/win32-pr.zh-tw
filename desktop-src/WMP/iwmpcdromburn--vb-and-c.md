---
title: 'IWMPCdromBurn (VB 和 C ) 介面 (h.264. h) '
description: 提供用來管理建立音訊 Cd 的屬性和方法。
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- IWMPCdromBurn (VB 和 C ) 介面 Windows Media Player
- IWMPCdromBurn (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPCdromBurn (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fe21a20194f57e4a8b52a3ba05032a07cb31f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998657"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>IWMPCdromBurn (VB 和 c # ) 介面

提供用來管理建立音訊 Cd 的屬性和方法。

## <a name="members"></a>成員

**IWMPCdromBurn (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPCdromBurn (VB 和 c # )** 介面都有這些方法。



| 方法                                                                             | 描述                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | 清除目前的 CD。<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | 抓取 CD 的指定屬性值。<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | 提供 CD 光碟機和媒體的相關資訊。<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | 更新目前燒錄播放清單的狀態資訊。<br/> |
| [**startBurn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | 燒錄 CD。<br/>                                                 |
| [**stopBurn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | 停止 CD 燒錄流程。<br/>                                 |



 

### <a name="properties"></a>屬性

**IWMPCdromBurn (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                    | 存取類型          | Description                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | 唯讀<br/> | 取得值，這個值表示要燒錄的 CD 類型。<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | 唯讀<br/> | 取得要燒錄到 CD 的目前播放清單。<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | 唯讀<br/> | 取得完成百分比的 CD 燒錄進度。<br/>                |
| [**burnState**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | 唯讀<br/> | 取得列舉值，這個值表示目前的燒錄狀態。<br/> |
| [**標籤**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | 唯讀<br/> | 取得 CD 磁片區標籤字串。<br/>                                 |



 

轉換您要燒錄之 CD 的 **IWMPCdrom** 介面，以取得 **IWMPCdromBurn** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





