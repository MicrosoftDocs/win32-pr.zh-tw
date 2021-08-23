---
description: 代表檔案歷程記錄重新關聯功能，可讓使用者重新建立與過去相同使用者所使用的備份目標的關聯性。 重新關聯是藉由呼叫 IFhReassociation 介面的方法來執行。
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: 'FhReassociation 類別 (Fhcfg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: f4b8cb55ce4b374f7f17f16044811a930623fc777a028ee98b5d8726bf714cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538508"
---
# <a name="fhreassociation-class"></a>FhReassociation 類別

代表檔案歷程記錄重新關聯功能，可讓使用者重新建立與過去相同使用者所使用的備份目標的關聯性。 重新關聯是藉由呼叫 [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) 介面的方法來執行。

## <a name="when-to-implement"></a>執行時機

檔案歷程記錄 API 會執行這個類別。 若要建立這個類別的實例，請使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Fhcfg。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Fhcfg .idl</dt> </dl> |



 

 
