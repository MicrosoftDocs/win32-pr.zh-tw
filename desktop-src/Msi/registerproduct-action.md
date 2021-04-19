---
description: RegisterProduct 動作會向安裝程式和 [新增/移除程式] 註冊產品資訊。 此外，此動作會將 Windows Installer 資料庫封裝儲存在本機電腦上。
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: RegisterProduct 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993120"
---
# <a name="registerproduct-action"></a>RegisterProduct 動作

RegisterProduct 動作會向安裝程式和 [新增/移除程式] 註冊產品資訊。 此外，此動作會將 Windows Installer 資料庫封裝儲存在本機電腦上。

RegisterProduct 動作會設定主控台中的 [新增/移除程式] 所顯示的控制項。 如需詳細資訊，請參閱 [使用 Windows Installer 設定 [新增/移除程式](configuring-add-remove-programs-with-windows-installer.md)]。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述            |
|-------|---------------------------------------|
| \[1\] | 已註冊產品的相關資訊。 |



 

## <a name="remarks"></a>備註

在安裝期間，系統管理安裝點不會執行 RegisterProduct 動作。

 

 



