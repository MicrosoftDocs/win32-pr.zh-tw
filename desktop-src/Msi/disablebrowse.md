---
description: 將每部電腦系統原則的值設定為 &\# 0034; 1&\# 0034; 防止非系統管理員的使用者使用 [流覽] 對話方塊來找出儲存在媒體上的受管理應用程式來源，例如 cd-rom。
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991688"
---
# <a name="disablebrowse"></a>DisableBrowse

將此每部電腦 [系統原則](system-policy.md) 的值設定為 "1"，可防止非系統管理員的使用者使用 [[流覽] 對話方塊](browse-dialog.md) 來找出儲存在媒體上的 [*受管理應用程式*](m-gly.md) 來源，例如 cd-rom。 直接輸入的 [使用功能來源：] 下拉式方塊已鎖定，而 [流覽 ...]按鈕已停用。 如需有關來源流覽的詳細資訊，請參閱 [來源復原](source-resiliency.md)。

DisableBrowse 會覆寫 AllowLockdownBrowse 並防止流覽，即使已設定 AllowLockdownBrowse 也是如此。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="remarks"></a>備註

在 DisableBrowse 設定的某些情況下，非管理使用者可能仍然能夠從正確標示的媒體上的來源安裝受控應用程式。 設定 DisableBrowse 原則只會停用流覽至來源的功能。 您可以使用它來防止非系統管理員的使用者在安裝隨選安裝、重新安裝或修復期間流覽至新的來源。 如果設定了 [AllowLockdownMedia](allowlockdownmedia.md) ，則非管理的使用者仍然可以從正確標示的媒體安裝受控應用程式。

DisableBrowse 可防止非管理員使用者流覽至新的媒體位置或任何其他來源位置。 如需如何保護受控應用程式之媒體來源的詳細資訊，請參閱 [來源復原](source-resiliency.md)。

如需此原則與安裝來源互動的詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。

 

 



