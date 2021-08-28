---
description: 使用提升的 (系統) 許可權安裝 Windows Installer 套件。
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc015dad8096db16d8b70238a5fd7e07544b83f9a9e3d1a5045be9d12bbb30cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650238"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

您可以使用 AlwaysInstallElevated 原則，以提升的 (系統) 許可權來安裝 Windows Installer 套件。

* * 警告： * *

此選項相當於授與完整的系統管理許可權，而這可能會造成大量的安全性風險。 Microsoft 強烈不鼓勵使用此設定。

若要安裝具有提高許可權 (系統) 許可權的封裝，請在下列兩個登錄機碼底下將 AlwaysInstallElevated 值設為 "1"：

**HKEY \_\_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **安裝程式** 的目前使用者軟體原則

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

如果上述兩個登錄機碼底下的 AlwaysInstallElevated 值未設為 "1"，則安裝程式會使用較高的許可權來安裝受控應用程式，並針對未受管理的應用程式使用目前使用者的許可權層級。

因為此原則允許使用者安裝需要存取使用者可能沒有許可權來存取目錄和登錄機碼的應用程式，所以您應該考慮它是否為您的使用者提供適當的安全性層級。 設定此原則會指示 Windows Installer 在系統上安裝應用程式時使用系統許可權。 如果未設定此原則，系統會使用使用者的許可權來安裝未由系統管理員散發的應用程式，而且只有受管理的應用程式才會取得較高的許可權。

請注意，一旦啟用 AlwaysInstallElevated 的每一電腦原則，任何使用者都可以設定其每個使用者的設定。

## <a name="remarks"></a>備註

如需此原則與安裝來源互動的詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 



