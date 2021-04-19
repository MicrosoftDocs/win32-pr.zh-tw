---
description: 除了透過 >ivssbackupcomponents 介面透過其複本的裝置物件來存取之外，要求者也可以將陰影複製提供給其他進程使用，做為掛接的唯讀裝置。
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: 公開及呈現陰影複製的磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985701"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>公開及呈現陰影複製的磁片區

除了透過 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面透過其複本的 [*裝置物件*](vssgloss-d.md)來存取之外，要求者也可以將陰影複製提供給其他進程使用，做為掛接的唯讀裝置。

此程式稱為 [*公開陰影複製*](vssgloss-e.md)，並使用 [**>ivssbackupcomponents：： ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) 方法執行。

陰影複製可以公開為本機磁片區—指派磁碟機號或與掛接的資料夾相關聯，或作為檔案共用。

為了說明這一點，請考慮在掛接于 F：的系統 exposedSys 上的磁片區所組成的陰影複製， \\ 其根目錄為 dirOne 和 dirTwo 目錄，以及檔案 >fileone.txt。

## <a name="exposing-a-shadow-copy-locally"></a>在本機公開陰影複製

掛接為本機磁片區時，陰影複製的根目錄一律會顯示在掛接點 (磁碟機號或掛接的資料夾) ，而且所有陰影複製的檔案都是可見的。

如果陰影複製是透過掛接的資料夾 C： ShadowOfF 在本機公開的 \\ ，您會發現磁片上的所有檔案都掛接于 F： \\ 于 C： ShadowOfF 下提供的陰影複製時 \\ 。 檢查 C： \\ ShadowOfF 會顯示兩個目錄（dirOne 和 dirTwo），以及 c： ShadowOfF 下的一個檔案（>fileone.txt） \\ 。

在本機公開陰影複製的呼叫可能是：

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

如果已成功在本機公開陰影複製， *wszExposed* 應該包含寬字元字串 "C： \\ ShadowOfF"。

您稍後可以藉由呼叫 [**IVssBackupComponentsEx2：： UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot)，將陰影複製未公開。

只有持續性陰影複製（也就是以 VSS \_ CTX \_ NAS \_ 復原或 vss CTX 應用程式回復所建立的陰影複製 \_ \_ \_ ）可以在本機公開。

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>將陰影複製公開為遠端共用

或者，您也可以選擇將磁片的陰影複製設為 F： \\ 提供作為遠端檔案共用，並只將 dirTwo 下的資料公開為檔案共用 dirTwoOfF。

在此情況下，系統可以將 \\ \\ \\ exposedSys \\ dirTwoOfF 對應為網路磁碟機機，以存取 F： dirTwo 下的檔案陰影複製。

執行遠端將陰影複製公開為共用的呼叫可能如下所示：

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

如果已成功從遠端公開陰影複製， *wszExposed* 應該包含寬字元字串 "dirTwoOfF"。

任何目前對應 dirTwoOfF 網路共用的系統都可以中斷連線，就像它可能與任何一般共用中斷連線一樣。

## <a name="surfacing-a-shadow-copy"></a>呈現陰影複製

[*呈現的陰影複製*](vssgloss-s.md)是系統的 Mount Manager 命名空間已知的陰影複製。

這表示，您可以使用 **FindFirstVolume** 和 **FindNextVolume**，找出這類陰影複製的方式，就像是尋找任何其他可用但尚未載入的磁片區。

顯然，公開的陰影複製也會呈現陰影複製。 不過，反向並不一定是 true。

如果已卸載本機公開的陰影複製，或系統選擇中斷遠端公開陰影複製的連接，則不會再公開陰影複製。 不過，只要保存陰影複製，就會顯示磁片區。 這表示它們可以像任何其他唯讀磁片區一樣掛接。

 

 



