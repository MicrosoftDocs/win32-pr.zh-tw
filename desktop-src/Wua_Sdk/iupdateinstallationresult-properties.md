---
description: IUpdateInstallationResult 介面會定義下列屬性。
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: IUpdateInstallationResult 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7574d6fd84afc737d67147c8b40e1e501857f6c19d69bcce4b4b7216bb9c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994408"
---
# <a name="iupdateinstallationresult-properties"></a>IUpdateInstallationResult 屬性

[**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)介面會定義下列屬性。



| 屬性                                                           | 描述                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | 取得在更新作業期間引發的 **HRESULT** 例外狀況值。                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | 取得布林值，指出電腦上是否需要重新開機系統才能完成更新的安裝。 |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | 取得 [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) 值，這個值會指定更新的作業結果。          |



 

 

 



