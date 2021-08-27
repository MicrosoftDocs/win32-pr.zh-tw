---
description: 表示建立 FhConfigMgr 物件時所使用之使用者的檔案歷程記錄設定。 所有設定作業都是藉由呼叫 IFhConfigMgr 介面的方法來執行。
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: 'FhConfigMgr 類別 (Fhcfg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 700e96b72e3b23fa83a384a68bd2723ae244d69b0b10ed47db10843793166f40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058968"
---
# <a name="fhconfigmgr-class"></a>FhConfigMgr 類別

表示建立 **FhConfigMgr** 物件時所使用之使用者的檔案歷程記錄設定。 所有設定作業都是藉由呼叫 [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) 介面的方法來執行。

## <a name="when-to-implement"></a>執行時機

檔案歷程記錄 API 會執行這個類別。 若要建立這個類別的實例，請使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Fhcfg。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Fhcfg .idl</dt> </dl> |



 

 
