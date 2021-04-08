---
title: IReconcileInitiator 介面
description: 公開方法，這些方法會提供公事包調整器，以通知起始端的進度、設定終止物件，以及要求指定的檔版本。 啟動器負責執行這個介面。
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- IReconcileInitiator 介面舊版 Windows 環境功能
- IReconcileInitiator 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685932"
---
# <a name="ireconcileinitiator-interface"></a>IReconcileInitiator 介面

公開方法，這些方法會提供公事包調整器，以通知起始端的進度、設定終止物件，以及要求指定的檔版本。 啟動器負責執行這個介面。

## <a name="members"></a>成員

**IReconcileInitiator** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IReconcileInitiator** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IReconcileInitiator** 介面具有這些方法。



| 方法                                                                 | 描述                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | 設定可讓啟動器以非同步方式終止對帳的物件。 公事包調整器通常會針對冗長或牽涉到使用者互動的對帳設定此物件。 <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | 指出公事包調整器完成對帳所進行的進度量。 此數量為分數，而且會計算為 *ulProgress* 和 *ulProgressMax* 參數的商。 Reconcilers 應該在其對帳程式期間定期呼叫這個方法。 <br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.0 版或更新版本) </dt> </dl> |



 

