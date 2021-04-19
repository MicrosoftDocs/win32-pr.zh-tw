---
description: 由應用程式用來列舉專案樹狀結構目前資料夾中的 IWiaItem2 物件。
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: 'IEnumWiaItem2 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972466"
---
# <a name="ienumwiaitem2-interface"></a>IEnumWiaItem2 介面

由應用程式用來列舉專案樹狀結構目前資料夾中的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。

## <a name="members"></a>成員

**IEnumWiaItem2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumWiaItem2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumWiaItem2** 介面具有這些方法。



| 方法                                          | 描述                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**克隆**](-wia-ienumwiaitem2-clone.md)       | 建立 **IEnumWiaItem2** 介面的其他實例，並將指標傳回給它。 <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | 傳回這個列舉值所儲存的元素數目。 <br/>                                                          |
| [**下一步**](-wia-ienumwiaitem2-next.md)         | 填滿 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標陣列。<br/>                                       |
| [**重設**](-wia-ienumwiaitem2-reset.md)       | 將列舉參考重設為第一個 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。 <br/>                          |
| [**跳過**](-wia-ienumwiaitem2-skip.md)         | 在列舉可用的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件期間略過指定數目的專案。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
