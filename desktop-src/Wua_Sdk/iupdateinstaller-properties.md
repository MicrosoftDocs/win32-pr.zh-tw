---
description: IUpdateInstaller 介面會定義下列屬性。
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: IUpdateInstaller 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c6076e395e98ef21cd54fbf45ffdc5e57bc29fa8ceffc78c16d9a9a0d2bc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049146"
---
# <a name="iupdateinstaller-properties"></a>IUpdateInstaller 屬性

[**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)介面會定義下列屬性。



| 屬性                                                                                      | 描述                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | 取得和設定布林值，這個值會指出是否要在安裝更新時，對使用者顯示來源提示。                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | 取得和設定目前的用戶端應用程式。                                                                                         |
| [**System.componentmodel.backgroundworker.isbusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | 取得布林值，指出電腦是否在特定時間進行安裝或卸載。        |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | 取得或設定布林值，指出是否強制安裝或卸載更新。                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | 取得和設定可包含對話方塊的父視窗的控制碼。                                                            |
| [**ParentWindow**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | 取得和設定介面，這個介面表示可以包含對話方塊的父視窗。                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | 取得布林值，這個值表示安裝或卸載更新之前是否需要重新開機系統。                   |
| [**更新**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | 取得和設定介面，其中包含指定用於安裝或卸載之更新的唯讀集合。 |



 

 

 



