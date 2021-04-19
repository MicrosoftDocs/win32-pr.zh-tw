---
description: ITAttributeList 介面會提供方法來取得和設定未中斷的屬性。
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: 'ITAttributeList 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994871"
---
# <a name="itattributelist-interface"></a>ITAttributeList 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITAttributeList** 介面會提供方法來取得和設定未中斷的屬性。 關於會話描述項通訊協定中的屬性字串位置 (SDP，請參閱 RFC 2327) 封包，方法會假設所有屬性字串都存在於指定媒體屬性之前，以及在所有通用屬性之後。 **ITAttributeList** 介面是藉由在 [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)上呼叫 **QueryInterface** 來建立。

## <a name="members"></a>成員

**ITAttributeList** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITAttributeList** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITAttributeList** 介面具有這些方法。



| 方法                                                          | 描述                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**添加**](itattributelist-add.md)                              | 將屬性加入指定的索引處。<br/>   |
| [**刪除**](itattributelist-delete.md)                        | 刪除指定索引處的屬性<br/> |
| [**取得 \_ AttributeList**](itattributelist-get-attributelist.md) | 取得屬性清單。<br/>                 |
| [**取得 \_ 計數**](itattributelist-get-count.md)                 | 取得屬性的數目。<br/>               |
| [**取得 \_ 專案**](itattributelist-get-item.md)                   | 取得索引所指定的屬性。<br/>   |
| [**put \_ AttributeList**](itattributelist-put-attributelist.md) | 設定屬性的清單。<br/>                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

