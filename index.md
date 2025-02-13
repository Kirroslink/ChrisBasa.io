import React from 'react';
import { Github, Twitter, Mail, Linkedin } from 'lucide-react';

const MinimalLanding = () => {
  const links = [
    {
      title: 'GitHub',
      url: 'https://github.com/yourusername',
      icon: <Github className="w-5 h-5" />
    },
    {
      title: 'Twitter',
      url: 'https://twitter.com/yourusername',
      icon: <Twitter className="w-5 h-5" />
    },
    {
      title: 'LinkedIn',
      url: 'https://linkedin.com/in/yourusername',
      icon: <Linkedin className="w-5 h-5" />
    },
    {
      title: 'Email',
      url: 'mailto:you@example.com',
      icon: <Mail className="w-5 h-5" />
    }
  ];

  return (
    <div className="min-h-screen bg-gradient-to-b from-gray-100 to-gray-200 flex flex-col items-center py-16 px-4">
      <div className="w-full max-w-md">
        {/* Profile Section */}
        <div className="flex flex-col items-center mb-8">
          <div className="w-24 h-24 rounded-full bg-gray-300 mb-4 overflow-hidden">
            <img
              src="/api/placeholder/96/96"
              alt="Profile"
              className="w-full h-full object-cover"
            />
          </div>
          <h1 className="text-2xl font-bold text-gray-800 mb-2">Your Name</h1>
          <p className="text-gray-600 text-center mb-4">
            Short bio about yourself. What you do, what you're passionate about.
          </p>
        </div>

        {/* Links Section */}
        <div className="space-y-4">
          {links.map((link, index) => (
            <a
              key={index}
              href={link.url}
              target="_blank"
              rel="noopener noreferrer"
              className="flex items-center justify-between p-4 bg-white rounded-lg shadow-sm hover:shadow-md transition-shadow duration-200 group"
            >
              <div className="flex items-center space-x-3">
                {link.icon}
                <span className="font-medium text-gray-700 group-hover:text-gray-900">
                  {link.title}
                </span>
              </div>
              <svg
                className="w-5 h-5 text-gray-400 group-hover:text-gray-600"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  strokeLinecap="round"
                  strokeLinejoin="round"
                  strokeWidth={2}
                  d="M9 5l7 7-7 7"
                />
              </svg>
            </a>
          ))}
        </div>
      </div>
    </div>
  );
};

export default MinimalLanding;
