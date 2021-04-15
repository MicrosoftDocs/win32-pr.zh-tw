---
description: 提供與交易相關之內容物件屬性的存取權。
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: ICoNtextTransactionInfo 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468305"
---
# <a name="icontexttransactioninfo-interface"></a>ICoNtextTransactionInfo 介面

提供與交易相關之內容物件屬性的存取權。

## <a name="when-to-implement"></a>執行時機

您不應該執行這個介面。 標準實作為提供完整的功能。

## <a name="when-to-use"></a>使用時機

您可以使用這個介面來存取與交易相關的內容物件屬性。

## <a name="members"></a>成員

**ICoNtextTransactionInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ICoNtextTransactionInfo** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ICoNtextTransactionInfo** 介面具有這些方法。



| 方法                                                                                         | 描述                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**FetchTransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | 抓取與目前內容相關聯的交易或交易 proxy （如果有的話）。<br/>              |
| [**GetTxIsolationLevelAndTimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | 抓取根交易內容中所裝載之交易的隔離等級和超時值。<br/> |
| [**RegisterTransactionProxy**](icontexttransactioninfo-fetchtransaction.md)                   | 將 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 的執行與目前的內容產生關聯。<br/>            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/> |



 

