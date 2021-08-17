---
description: RegisterProduct 動作會向安裝程式和 [新增/移除程式] 註冊產品資訊。 此外，此動作會將 Windows Installer 資料庫封裝儲存在本機電腦上。
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: RegisterProduct 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185b670b7a24c31e6dc5adb402cd6c557e2eba9eac3db5138744cd1e827113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375959"
---
# <a name="registerproduct-action"></a>RegisterProduct 動作

RegisterProduct 動作會向安裝程式和 [新增/移除程式] 註冊產品資訊。 此外，此動作會將 Windows Installer 資料庫封裝儲存在本機電腦上。

RegisterProduct 動作會設定主控台中的 [新增/移除程式] 所顯示的控制項。 如需詳細資訊，請參閱[使用 Windows Installer 設定 [新增/移除程式](configuring-add-remove-programs-with-windows-installer.md)]。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述            |
|-------|---------------------------------------|
| \[1\] | 已註冊產品的相關資訊。 |



 

## <a name="remarks"></a>備註

在安裝期間，系統管理安裝點不會執行 RegisterProduct 動作。

 

 



