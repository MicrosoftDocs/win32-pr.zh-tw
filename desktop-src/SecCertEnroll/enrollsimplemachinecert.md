---
description: 使用範本、憑證顯示名稱和憑證描述，在證書階層中註冊電腦。
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977064"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

EnrollSimpleMachineCert 範例會使用範本、憑證顯示名稱和憑證描述，在證書階層中註冊電腦。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，根據預設，系統會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ EnrollSimpleMachineCert 資料夾中安裝 c + + 版本的範例。 VBScript 版本安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VBS \\ EnrollSimpleMachineCert 資料夾中。

## <a name="discussion"></a>討論

EnrollSimpleMachineCert 範例：

1.  處理命令列引數。 命令列應該包含範本的名稱、憑證顯示名稱和憑證描述。
2.  建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，並使用命令列上指定的範本將它初始化。 第一個參數的 CoNtextAdministratorForceMachine 值指定由代表電腦的系統管理員要求憑證。
3.  將顯示名稱和描述新增至註冊物件。
4.  嘗試註冊憑證要求，並檢查進程的狀態。 CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 



