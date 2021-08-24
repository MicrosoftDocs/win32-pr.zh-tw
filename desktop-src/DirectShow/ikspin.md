---
description: IKsPin 介面會提供方法，以在核心模式篩選器上取出 pin 所支援的媒體。 除了此處所示的 IKsPin 之外，還有其他方法，但 DirectShow 不支援。
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: 'IKsPin 介面 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 8855378544bcc2ea7357af220b5d80d32edde74a50c304e973c9821aa8e9a41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792328"
---
# <a name="ikspin-interface"></a>IKsPin 介面

`IKsPin`介面會提供方法，以在核心模式篩選器上取得 pin 所支援的媒體。 `IKsPin`除了此處所示的以外，還有其他方法，但 DirectShow 不支援。

## <a name="members"></a>成員

**IKsPin** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IKsPin** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IKsPin** 介面具有這些方法。



| 方法                                          | 描述                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | 抓取 pin 所支援的媒體。<br/> |



 

## <a name="remarks"></a>備註

您必須在 Ksproxy 之前包含 Ks。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Ksproxy。h</dt> </dl>    |
| 程式庫<br/>                  | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
