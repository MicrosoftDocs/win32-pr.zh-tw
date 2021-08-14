---
title: 'INapSoHProcessor 介面 (NapProtocol .h) '
description: Sha 用來處理 SoHResponses 和 Shv 的內容，以處理 SoHRequests 的內容。
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- INapSoHProcessor 介面 NAP
- INapSoHProcessor 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca4a87e15d3810605038231eaec066e9f26ed079aca0d0715c72e7c69ed8d600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799480"
---
# <a name="inapsohprocessor-interface"></a>INapSoHProcessor 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHProcessor** 會提供方法，讓 sha 用來處理 [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh)的內容，以及由 shv 處理 **SoHRequests** 內容。

## <a name="members"></a>成員

**INapSoHProcessor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapSoHProcessor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSoHProcessor** 介面具有這些方法。



| 方法                                                                                           | 描述                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | 尋找下一個 SoH 封包屬性的位置索引。<br/>                 |
| [**INapSoHProcessor：： GetAttribute**](inapsohprocessor-getattribute-method.md)                   | 抓取屬性型別和值。<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | 捕獲 SoH 中包含的屬性數目。<br/>                   |
| [**INapSoHProcessor：： Initialize**](inapsohprocessor-initialize-method.md)                       | 初始化 SoH 通訊協定封包和 NAP 系統以進行內容處理。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

