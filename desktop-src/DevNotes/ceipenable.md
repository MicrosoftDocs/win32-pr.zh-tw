---
description: HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable。
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687e17bf5438406fb7a29b954bf8a2640fc0ea5d193ba49ae7fd7bd02f1f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956117"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| 資料類型  | 範圍                     | 預設值 |
|------------|---------------------------|---------------|
| REG \_ DWORD | 0 (停用) 或 1 (啟用)  | 0             |



 

## <a name="description"></a>描述

啟用 Windows 的客戶經驗改進計畫。

## <a name="change-method"></a>變更方法

若要變更這個專案的值，請在 [主控台中，選取 [ **系統和維護**]，然後選取 [ **問題報告與解決方案**]。 按一下 [另請參閱] 區段中的 [**客戶經驗改進設定**]。

## <a name="activation-method"></a>啟用方法

對此專案所做的變更會立即生效。 啟用此登錄機碼會讓整個電腦啟用 Windows 客戶經驗改進計畫。 停用此登錄機碼會導致整個電腦的 Windows 客戶經驗改進計畫停用。

在支援群組原則的系統上，群組原則設定會取代此專案。 雖然已啟用 Windows 客戶經驗改進計畫 CEIP 啟用群組原則設定，但系統會忽略此專案。 此原則設定的設定會儲存在 [ **HKLM \\ Software policy \\ \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**] 底下的 [**原則**] 區段中。

 

 



