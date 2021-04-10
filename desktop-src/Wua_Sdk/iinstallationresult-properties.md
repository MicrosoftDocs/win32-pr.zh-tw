---
description: IInstallationResult 介面會定義下列屬性。
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: IInstallationResult 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026278"
---
# <a name="iinstallationresult-properties"></a>IInstallationResult 屬性

[**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)介面會定義下列屬性。



| 屬性                                                     | 描述                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | 取得安裝期間引發之例外狀況的 **HRESULT** （如果有的話）。                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | 取得布林值，指出您是否必須重新開機電腦，才能完成安裝或卸載更新。 |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | 取得 [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) 值，這個值會指定更新的作業結果。               |



 

 

 



