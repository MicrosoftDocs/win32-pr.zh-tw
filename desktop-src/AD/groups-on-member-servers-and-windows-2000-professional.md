---
title: 成員伺服器與 Windows 2000 Professional 上的群組
description: 在執行 Windows 2000 Professional 的成員伺服器和電腦上，有一個本機安全性資料庫。
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- 成員伺服器與 Windows 2000 Professional AD 的群組
- 群組 AD、成員伺服器上的群組和 Windows 2000 專業版
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300120"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>成員伺服器與 Windows 2000 Professional 上的群組

在執行 Windows 2000 Professional 的成員伺服器和電腦上，有一個本機安全性資料庫。 這個本機安全性資料庫可以包含自己的本機使用者和本機群組，而該群組的範圍只是建立它們的特定電腦。 在成員伺服器上管理這些類型的使用者和群組，以及在 Windows NT 工作站或 Windows 2000 Professional 上執行的電腦上，請使用 WinNT 提供者。

當成員伺服器或在 Windows 2000 Professional 或 Windows 2000 Professional 上執行的電腦是 Windows 2000 網域的成員時，網域中的群組或使用者可以在本機安全性資料庫中使用，將許可權授與該特定電腦上的該群組。

使用 ADSI 在 Windows 2000 網域上管理群組時，請使用 LDAP 提供者。 當您在 Windows NT 工作站或 Windows 2000 Professional 上執行的成員伺服器和電腦上管理群組時，請使用 WinNT 提供者。

您至少必須系結至每個提供者： 1) 系結至 LDAP 提供者，以取得您想要新增至本機資料庫群組的群組或使用者的 ADsPath，以及 2) 系結至 WinNT 提供者，以將該使用者或群組新增至本機群組。

 

 




