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
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847270"
---
# <a name="fhconfigmgr-class"></a>FhConfigMgr 類別

表示建立 **FhConfigMgr** 物件時所使用之使用者的檔案歷程記錄設定。 所有設定作業都是藉由呼叫 [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) 介面的方法來執行。

## <a name="when-to-implement"></a>執行時機

檔案歷程記錄 API 會執行這個類別。 若要建立這個類別的實例，請使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Fhcfg。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Fhcfg .idl</dt> </dl> |



 

 
