---
title: WinNT 物件類別階層
description: WinNT 物件類別階層從 Namespace 物件開始。
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- WinNT 服務提供者 ADSI、物件類別階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507024"
---
# <a name="winnt-object-class-hierarchy"></a>WinNT 物件類別階層

WinNT 物件類別階層從 Namespace 物件開始。



| Object 類別                   | Description                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| 命名空間<br/>           | 最上層物件容器。<br/>                                            |
| 網域<br/>              | Windows NT 網域。<br/>                                                 |
| User<br/>                | 使用者帳戶。<br/>                                                          |
| Group<br/>               | 用於管理存取權限的群組帳戶。<br/>                              |
| UserGroupCollection<br/> | 一組執行 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)的使用者群組。<br/>  |
| GroupCollection<br/>     | 一組執行 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)的其他群組。<br/> |
| 電腦<br/>            | Windows NT 4.0 伺服器或工作站。<br/>                                  |
| PrintJob<br/>            | 列印佇列中的列印工作。<br/>                                          |
| PrintJobsCollection<br/> | 一組列印工作。<br/>                                                   |
| PrintQueue<br/>          | 列印印表機多工緩衝處理程式上的佇列。<br/>                                      |
| 服務<br/>             | 以服務方式執行的應用程式。<br/>                                      |
| FileService<br/>         | 存取檔案系統的服務。<br/>                                        |
| FileShare<br/>           | 檔案共用點。<br/>                                                      |
| 資源<br/>            | 服務中的資源。<br/>                                             |
| 工作階段<br/>             | 作用中的檔案服務連接。<br/>                                     |
| User<br/>                | 本機使用者帳戶。<br/>                                                    |
| Group<br/>               | 本機群組。<br/>                                                           |
| UserCollection<br/>      | 本機使用者的集合。<br/>                                             |
| GroupCollection<br/>     | 本機群組的集合。<br/>                                            |
| 結構描述<br/>              | WinNT 架構容器。<br/>                                                |
| 類別<br/>               | 架構類別定義。<br/>                                               |
| 屬性<br/>            | 架構屬性定義。<br/>                                           |
| Syntax<br/>              | 屬性的語法。<br/>                                                  |



 

 

 





