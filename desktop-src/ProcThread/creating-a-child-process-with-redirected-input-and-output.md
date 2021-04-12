---
description: 本主題中的範例將示範如何使用來自主控台進程的 CreateProcess 函數來建立子進程。
ms.assetid: a4e37069-2b3a-4b6d-9cfd-eb1700ab3bc6
title: 使用重新導向的輸入和輸出來建立子程序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a8e922c37baf20dae2d3a26b8cd0705e4c1a5
ms.sourcegitcommit: 005593a756bad634e35a57e4fea9167566d4a550
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/01/2021
ms.locfileid: "104195639"
---
# <a name="creating-a-child-process-with-redirected-input-and-output"></a><span data-ttu-id="57a53-103">使用重新導向的輸入和輸出來建立子程序</span><span class="sxs-lookup"><span data-stu-id="57a53-103">Creating a Child Process with Redirected Input and Output</span></span>

<span data-ttu-id="57a53-104">本主題中的範例將示範如何使用來自主控台進程的 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數來建立子進程。</span><span class="sxs-lookup"><span data-stu-id="57a53-104">The example in this topic demonstrates how to create a child process using the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function from a console process.</span></span> <span data-ttu-id="57a53-105">它也會示範使用匿名管道來重新導向子進程標準輸入和輸出控制碼的技巧。</span><span class="sxs-lookup"><span data-stu-id="57a53-105">It also demonstrates a technique for using anonymous pipes to redirect the child process's standard input and output handles.</span></span> <span data-ttu-id="57a53-106">請注意，具名管道也可以用來重新導向進程 i/o。</span><span class="sxs-lookup"><span data-stu-id="57a53-106">Note that named pipes can also be used to redirect process I/O.</span></span>

<span data-ttu-id="57a53-107">[**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)函式會使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構，建立兩個管道的讀取和寫入端的可繼承控制碼。</span><span class="sxs-lookup"><span data-stu-id="57a53-107">The [**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe) function uses the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to create inheritable handles to the read and write ends of two pipes.</span></span> <span data-ttu-id="57a53-108">一個管道的讀取端可作為子進程的標準輸入，而另一個管道的寫入端則是子進程的標準輸出。</span><span class="sxs-lookup"><span data-stu-id="57a53-108">The read end of one pipe serves as standard input for the child process, and the write end of the other pipe is the standard output for the child process.</span></span> <span data-ttu-id="57a53-109">這些管道控制碼是在 [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) 結構中指定的，因此子進程會繼承標準的控制碼。</span><span class="sxs-lookup"><span data-stu-id="57a53-109">These pipe handles are specified in the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure, which makes them the standard handles inherited by the child process.</span></span>

<span data-ttu-id="57a53-110">父進程會使用這兩個管道的另一端來寫入子進程的輸入，並從子進程的輸出中讀取。</span><span class="sxs-lookup"><span data-stu-id="57a53-110">The parent process uses the opposite ends of these two pipes to write to the child process's input and read from the child process's output.</span></span> <span data-ttu-id="57a53-111">如 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構中所指定，這些控制碼也是可繼承的。</span><span class="sxs-lookup"><span data-stu-id="57a53-111">As specified in the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure, these handles are also inheritable.</span></span> <span data-ttu-id="57a53-112">不過，這些控制碼不得被繼承。</span><span class="sxs-lookup"><span data-stu-id="57a53-112">However, these handles must not be inherited.</span></span> <span data-ttu-id="57a53-113">因此，在建立子進程之前，父進程會使用 [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation) 函式，以確保子進程標準輸入的寫入控制碼和子進程標準輸出的讀取控制碼無法被繼承。</span><span class="sxs-lookup"><span data-stu-id="57a53-113">Therefore, before creating the child process, the parent process uses the [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation) function to ensure that the write handle for the child process's standard input and the read handle for the child process's standard output cannot be inherited.</span></span> <span data-ttu-id="57a53-114">如需詳細資訊，請參閱 [管道](/windows/desktop/ipc/pipes)。</span><span class="sxs-lookup"><span data-stu-id="57a53-114">For more information, see [Pipes](/windows/desktop/ipc/pipes).</span></span>

<span data-ttu-id="57a53-115">以下是父進程的程式碼。</span><span class="sxs-lookup"><span data-stu-id="57a53-115">The following is the code for the parent process.</span></span> <span data-ttu-id="57a53-116">它會採用單一命令列引數：文字檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="57a53-116">It takes a single command-line argument: the name of a text file.</span></span>


```C++
#include <windows.h> 
#include <tchar.h>
#include <stdio.h> 
#include <strsafe.h>

#define BUFSIZE 4096 
 
HANDLE g_hChildStd_IN_Rd = NULL;
HANDLE g_hChildStd_IN_Wr = NULL;
HANDLE g_hChildStd_OUT_Rd = NULL;
HANDLE g_hChildStd_OUT_Wr = NULL;

HANDLE g_hInputFile = NULL;
 
void CreateChildProcess(void); 
void WriteToPipe(void); 
void ReadFromPipe(void); 
void ErrorExit(PTSTR); 
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   SECURITY_ATTRIBUTES saAttr; 
 
   printf("\n->Start of parent execution.\n");

// Set the bInheritHandle flag so pipe handles are inherited. 
 
   saAttr.nLength = sizeof(SECURITY_ATTRIBUTES); 
   saAttr.bInheritHandle = TRUE; 
   saAttr.lpSecurityDescriptor = NULL; 

// Create a pipe for the child process's STDOUT. 
 
   if ( ! CreatePipe(&g_hChildStd_OUT_Rd, &g_hChildStd_OUT_Wr, &saAttr, 0) ) 
      ErrorExit(TEXT("StdoutRd CreatePipe")); 

// Ensure the read handle to the pipe for STDOUT is not inherited.

   if ( ! SetHandleInformation(g_hChildStd_OUT_Rd, HANDLE_FLAG_INHERIT, 0) )
      ErrorExit(TEXT("Stdout SetHandleInformation")); 

// Create a pipe for the child process's STDIN. 
 
   if (! CreatePipe(&g_hChildStd_IN_Rd, &g_hChildStd_IN_Wr, &saAttr, 0)) 
      ErrorExit(TEXT("Stdin CreatePipe")); 

// Ensure the write handle to the pipe for STDIN is not inherited. 
 
   if ( ! SetHandleInformation(g_hChildStd_IN_Wr, HANDLE_FLAG_INHERIT, 0) )
      ErrorExit(TEXT("Stdin SetHandleInformation")); 
 
// Create the child process. 
   
   CreateChildProcess();

// Get a handle to an input file for the parent. 
// This example assumes a plain text file and uses string output to verify data flow. 
 
   if (argc == 1) 
      ErrorExit(TEXT("Please specify an input file.\n")); 

   g_hInputFile = CreateFile(
       argv[1], 
       GENERIC_READ, 
       0, 
       NULL, 
       OPEN_EXISTING, 
       FILE_ATTRIBUTE_READONLY, 
       NULL); 

   if ( g_hInputFile == INVALID_HANDLE_VALUE ) 
      ErrorExit(TEXT("CreateFile")); 
 
// Write to the pipe that is the standard input for a child process. 
// Data is written to the pipe's buffers, so it is not necessary to wait
// until the child process is running before writing data.
 
   WriteToPipe(); 
   printf( "\n->Contents of %S written to child STDIN pipe.\n", argv[1]);
 
// Read from pipe that is the standard output for child process. 
 
   printf( "\n->Contents of child process STDOUT:\n\n");
   ReadFromPipe(); 

   printf("\n->End of parent execution.\n");

// The remaining open handles are cleaned up when this process terminates. 
// To avoid resource leaks in a larger application, close handles explicitly. 

   return 0; 
} 
 
void CreateChildProcess()
// Create a child process that uses the previously created pipes for STDIN and STDOUT.
{ 
   TCHAR szCmdline[]=TEXT("child");
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bSuccess = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
// This structure specifies the STDIN and STDOUT handles for redirection.
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
   siStartInfo.hStdError = g_hChildStd_OUT_Wr;
   siStartInfo.hStdOutput = g_hChildStd_OUT_Wr;
   siStartInfo.hStdInput = g_hChildStd_IN_Rd;
   siStartInfo.dwFlags |= STARTF_USESTDHANDLES;
 
// Create the child process. 
    
   bSuccess = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   // If an error occurs, exit the application. 
   if ( ! bSuccess ) 
      ErrorExit(TEXT("CreateProcess"));
   else 
   {
      // Close handles to the child process and its primary thread.
      // Some applications might keep these handles to monitor the status
      // of the child process, for example. 

      CloseHandle(piProcInfo.hProcess);
      CloseHandle(piProcInfo.hThread);
      
      // Close handles to the stdin and stdout pipes no longer needed by the child process.
      // If they are not explicitly closed, there is no way to recognize that the child process has ended.
      
      CloseHandle(g_hChildStd_OUT_Wr);
      CloseHandle(g_hChildStd_IN_Rd);
   }
}
 
void WriteToPipe(void) 

// Read from a file and write its contents to the pipe for the child's STDIN.
// Stop when there is no more data. 
{ 
   DWORD dwRead, dwWritten; 
   CHAR chBuf[BUFSIZE];
   BOOL bSuccess = FALSE;
 
   for (;;) 
   { 
      bSuccess = ReadFile(g_hInputFile, chBuf, BUFSIZE, &dwRead, NULL);
      if ( ! bSuccess || dwRead == 0 ) break; 
      
      bSuccess = WriteFile(g_hChildStd_IN_Wr, chBuf, dwRead, &dwWritten, NULL);
      if ( ! bSuccess ) break; 
   } 
 
// Close the pipe handle so the child process stops reading. 
 
   if ( ! CloseHandle(g_hChildStd_IN_Wr) ) 
      ErrorExit(TEXT("StdInWr CloseHandle")); 
} 
 
void ReadFromPipe(void) 

// Read output from the child process's pipe for STDOUT
// and write to the parent process's pipe for STDOUT. 
// Stop when there is no more data. 
{ 
   DWORD dwRead, dwWritten; 
   CHAR chBuf[BUFSIZE]; 
   BOOL bSuccess = FALSE;
   HANDLE hParentStdOut = GetStdHandle(STD_OUTPUT_HANDLE);

   for (;;) 
   { 
      bSuccess = ReadFile( g_hChildStd_OUT_Rd, chBuf, BUFSIZE, &dwRead, NULL);
      if( ! bSuccess || dwRead == 0 ) break; 

      bSuccess = WriteFile(hParentStdOut, chBuf, 
                           dwRead, &dwWritten, NULL);
      if (! bSuccess ) break; 
   } 
} 
 
void ErrorExit(PTSTR lpszFunction) 

// Format a readable error message, display a message box, 
// and exit from the application.
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR)lpMsgBuf)+lstrlen((LPCTSTR)lpszFunction)+40)*sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR)lpDisplayBuf, TEXT("Error"), MB_OK); 

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
    ExitProcess(1);
}
```



<span data-ttu-id="57a53-117">以下是子進程的程式碼。</span><span class="sxs-lookup"><span data-stu-id="57a53-117">The following is the code for the child process.</span></span> <span data-ttu-id="57a53-118">它會使用 STDIN 和 STDOUT 的繼承控制碼來存取父系所建立的管道。</span><span class="sxs-lookup"><span data-stu-id="57a53-118">It uses the inherited handles for STDIN and STDOUT to access the pipe created by the parent.</span></span> <span data-ttu-id="57a53-119">父進程會從其輸入檔讀取，並將資訊寫入管道。</span><span class="sxs-lookup"><span data-stu-id="57a53-119">The parent process reads from its input file and writes the information to a pipe.</span></span> <span data-ttu-id="57a53-120">子系會使用 STDIN 透過管道接收文字，並使用 STDOUT 寫入至管道。</span><span class="sxs-lookup"><span data-stu-id="57a53-120">The child receives text through the pipe using STDIN and writes to the pipe using STDOUT.</span></span> <span data-ttu-id="57a53-121">父項會從管道的讀取端讀取，並將資訊顯示到其 STDOUT。</span><span class="sxs-lookup"><span data-stu-id="57a53-121">The parent reads from the read end of the pipe and displays the information to its STDOUT.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define BUFSIZE 4096 
 
int main(void) 
{ 
   CHAR chBuf[BUFSIZE]; 
   DWORD dwRead, dwWritten; 
   HANDLE hStdin, hStdout; 
   BOOL bSuccess; 
 
   hStdout = GetStdHandle(STD_OUTPUT_HANDLE); 
   hStdin = GetStdHandle(STD_INPUT_HANDLE); 
   if ( 
       (hStdout == INVALID_HANDLE_VALUE) || 
       (hStdin == INVALID_HANDLE_VALUE) 
      ) 
      ExitProcess(1); 
 
   // Send something to this process's stdout using printf.
   printf("\n ** This is a message from the child process. ** \n");

   // This simple algorithm uses the existence of the pipes to control execution.
   // It relies on the pipe buffers to ensure that no data is lost.
   // Larger applications would use more advanced process control.

   for (;;) 
   { 
   // Read from standard input and stop on error or no data.
      bSuccess = ReadFile(hStdin, chBuf, BUFSIZE, &dwRead, NULL); 
      
      if (! bSuccess || dwRead == 0) 
         break; 
 
   // Write to standard output and stop on error.
      bSuccess = WriteFile(hStdout, chBuf, dwRead, &dwWritten, NULL); 
      
      if (! bSuccess) 
         break; 
   } 
   return 0;
}
```



 

 
