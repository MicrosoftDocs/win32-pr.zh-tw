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
ms.openlocfilehash: ff81862e5ff0b27b75f952749957e6559306257240f2a02aca5f34e3efc870cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749138"
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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.0 版或更新版本) </dt> </dl> |



 

